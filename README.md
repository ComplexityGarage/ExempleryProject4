# TeaTemp Temperature Sensor
# Authors 
- Karolina Klimek
# Description of the project 
TeaTemp is a sensor to monitor the temperature of your hot drink. Imagine that you prepare a tea, at the beggining it is too hot for you to drink it, but if you wait too long finally it can get too cold. TeaTemp allows you to constantly monitor the temperature of the tea and drink your tea only when the temperature is suitable for you! 
# Science and tech used 
Parts needed to make TeaTemp sensor: <br />
- Seeed Studio XIAO ESP32C6 (https://wiki.seeedstudio.com/xiao_esp32c6_getting_started/) <br />
- Waterproof temperature sensor DS18B20 (https://botland.com.pl/sondy-wodoodporne/1713-sonda-wodoodporna-z-czujnikiem-temperatury-ds18b20-1m-5903351242226.html) <br />
- 4.7 kΩ resistor <br />
- Breadboard

Connection scheme is shown below:![image](https://github.com/user-attachments/assets/5fe416a5-7dfc-44ad-a2ea-5f58a9a82e8d) <br />
Connection scheme was made in WOKWI simulator (https://wokwi.com/). In the scheme non-waterproof version on DS18B20 temperature sensor is connected, however connections for waterproof version are the same. <br /> <br />
Code, which enables you to read the temperature from your sensor and send it through BLE bluetooth is available [here](./TeaTemp-code.ino). <br />
To use the code you need to download nessesary libraries. However there are incompatibilities between the OneWire library code and the ESP32 GPIO register definitions for the ESP32-C6 platform. One of the possible solutions to this issue is to go to \OneWire\util/OneWire_direct_gpio.h and edit the code. You need to find all instances of GPIO.in, GPIO.out_w1tc, GPIO.out_w1ts, GPIO.enable_w1tc, and GPIO.enable_w1ts. Then add .val to these registers to access their raw value. You can also just change /OneWire_direct_gpio.h file to the one, which is available [here](./OneWire_direct_gpio.h). <br /> <br />
Model of the package for the sensor is made of two parts bottom box and top box, .STL files for 3D printing are available in [STL_files](./STL_files/) directory. Models are designed for breadboard with 400 opennings ().

# State of the art 
TeaTemp, in it's first prototype version, allows you connect via BLE bluetooth with your smartphone and see the temperature on your phone. First you need to plug in the sensor using USB-C cable, then you can insert the waterproof sensor to your drink. To connect with the sensor you can use for example nRF Connect app, which is available both for android (https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=pl&pli=1) and IOS (https://apps.apple.com/pl/app/nrf-connect-for-mobile/id1054362403?l=pl). Instructions how to connect to the sensor and how to find the temperature are available [here](./How to connect to the sensor?.md).
# What next?
In the future it might be good to develop separate app, through which one could connect with the sensor. In addition to monitoring the drink temperature, in such application it might be nice to add for example functionality to set target temperature and when the drink reaches this temperature, app will send you the notification, that your drink is ready! Further improvements could aim at incorporating the sensor in the bottom of the cup to make it more comfortable for the users. It might be also interesting to add battery to the sensor and maybe even wireless charging. 
# Sources 
- Tutorial about BLE - https://www.youtube.com/watch?v=0Yvd_k0hbVs
- Website to create your own applications - https://appinventor.mit.edu/explore/ai2/tutorials
- Tutorial about creating a BLE app with MIT App Inventor - https://www.youtube.com/watch?v=RvbWl8rZOoQ&t=855s
