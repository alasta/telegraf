# Script to get Raspberry throttling :

mkdir /opt/scripts_telegraf  
wget https://raw.githubusercontent.com/alasta/telegraf/main/raspberry_monitoring/scripts/telegraf-rpi-get-throttled.sh -O /opt/scripts_telegraf/telegraf-rpi-get-throttled.sh  

chown -R telegraf:telegraf /opt/scripts_telegraf/  
chmod +x /opt/scripts_telegraf/telegraf-rpi-get-throttled.sh  



