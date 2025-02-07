# TeaTemp Temperature Sensor
# Authors 
- Karolina Klimek
# Description of the project 
TeaTemp is a sensor to monitor the temperature of your hot drink. Imagine that you boil water to prepare tea, at the beggining the tea is too hot for you to drink it, but if you wait too long finally it can get too cold. TeaTemp allows you to constantly monitor the temperature of the tea and drink your tea only when the temperature is suitable for you! 
# Science and tech used 
Parts needed to make TeaTemp sensor:
-Seeed Studio XIAO ESP32C6 (https://wiki.seeedstudio.com/xiao_esp32c6_getting_started/)
-Waterproof temperature sensor DS18B20 (https://botland.com.pl/sondy-wodoodporne/1713-sonda-wodoodporna-z-czujnikiem-temperatury-ds18b20-1m-5903351242226.html)
-4.7 kΩ resistor
-Breadboard
Connection scheme is shown here:![image](https://github.com/user-attachments/assets/5fe416a5-7dfc-44ad-a2ea-5f58a9a82e8d)

Code, which enables you to read the temperature from your sensor and send it through BLE bluetooth is available here.
# State of the art 
TeaTemp, in it's first prototype version, allows you connect via BLE bluetooth with your smartphone and see the temperature on your phone. First you need to plug in the sensor using USB-C cable, then you can insert the waterproof sensor to your drink. To connect with the sensor you can use for example nRF Connect app, which is available both for android (https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=pl&pli=1) and IOS (https://apps.apple.com/pl/app/nrf-connect-for-mobile/id1054362403?l=pl). You have to choose the divice and connect, then in properties you can see the temperature value. 
# What next?
In the future it might be good to develop separate app, through which one could connect with the sensor. In addition to monitoring the drink temperature, in such application it might be nice to add for example functionality to set target temperature and when the drink reaches this temperature, app sends you the notification, that your drink is ready! Further improvements could aim at incorporating the sensor in the bottom of the cup to make it more comfortable for the users. It might be also interesting to add battery to the sensor and maybe even wireless charging. 
# Sources 
- [Writing on GitHub] ( https://docs.github.com/en/get-started/writing-on-github ) 
