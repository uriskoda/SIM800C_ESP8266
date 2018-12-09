# Анатомия автозапуска 7.0
Anatomy of autorun 7.0

[Video with registration on the server and loading dashboard](https://www.youtube.com/watch?v=xgZZ417HFFQ)

[Video Firmware update, initial setup](https://youtu.be/zThLl6C_PjE)

****

MQTT broker

https://www.cloudmqtt.com

http://flyhub.org

******

MQTT apps on Android

[MQTT Dash Google Play](https://play.google.com/store/apps/details?id=net.routix.mqttdash&hl=ru) recommend

[IoT MQTT Panel](https://play.google.com/store/apps/details?id=snr.lab.iotmqttpanel.prod)

[IoT MQTT Dashboard](https://play.google.com/store/apps/details?id=com.thn.iotmqttdashboard)

[Linear MQTT Dashboard](https://play.google.com/store/apps/details?id=com.ravendmaster.linearmqttdashboard)

App Store: 

[IoT OnOff](https://itunes.apple.com/be/app/iot-onoff/id1267226555?mt=8)

***
Cloudmqtt.com > Log in> + Create Nwe Intance > 

**Name:** any name

**Plan:** Cute Cat(Free)

**Tags:** any name

**Data center:** EU-West-1 (Ireland) > Confirm > Create Nwe Intance

Details - Instance info - Copy: **Server, User, Password** and **Port**

********

Mqtt dash > Seting - Insert server settings: Server, User, Password and Port

Mqtt dash > Импорт/экспорт метрик: > ПОДПИСАТЬСЯ и ЖДАТЬ МЕТРИКИ.

*****

***Daschbord*** 

Cloudmqtt.com > Log in> WEBSOCKET UI > Websocket -Send message 

**Topic** metrics/exchange

**Message** >  https://raw.githubusercontent.com/martinhol221/SIM800C_ESP8266/master/daschbord.txt

*****

request **where?** to **topic car/c5/sub**	 returns  **car/c5/pub/gps**	52.834681,21.694131

request **money?** to **topic car/c5/sub**	 returns  **car/c5/pub/ussd** 2.87rub

request **signal?** to **topic car/c5/sub**	  returns **car/c5/pub/rssi**	29

request **wifion** to **topic car/c5/sub**	  Wi FI is turned on with the **Webasto_123456** access point

request **25** to **topic car/c5/sub/webasto**	  turns on relay K1 for 25 minutes

request **estart** to **topic car/c5/sub**	      includes relays K1, K2 and briefly K3

request **estop** to **topic car/c5/sub**	      disable all relays

request **ref** to **topic car/c5/sub**	      returns the data comes from the device to the phone in JSON format:

**{"pin":[11.73,0,0,0,0,0,0,0],"temp":[14.81,14.50,14.13],"time":[0,2day.18:28:24],"loss":[0,0,0]}**

{"pin":[Voltage, state K1, state K2, state K3, state K4, state K5, state IN1, state IN2],"temp":[temperature0, temperature1, temperature2],"time":[timer,Uptime],"loss":[0,0,error]}




