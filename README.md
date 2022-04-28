# telegraf
telegraf configuration.
  
# telegraf installation   
No package in default raspbian 11.  
Workaround : https://community.influxdata.com/t/installing-error-the-repository-https-repos-influxdata-com-raspbian-bullseye-release-does-not-have-a-release-file/22979  

```
sudo wget -qO- https://repos.influxdata.com/influxdb.key | sudo tee /etc/apt/trusted.gpg.d/influxdb.asc >/dev/null  
  
sudo echo "deb https://repos.influxdata.com/debian bullseye stable" | sudo tee /etc/apt/sources.list.d/influxdb.list  
  
sudo apt update  
  
sudo apt install telegraf  
  
## To collect  gpu temperature
sudo usermod -a -G video telegraf


##test with user telegraf to identify error/permission issues
telegraf -config /etc/telegraf/telegraf.conf -test

##test specific  
sudo -u telegraf telegraf --input-filter=disk --test
```
