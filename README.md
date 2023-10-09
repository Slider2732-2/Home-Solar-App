# Home-Solar-App
A simple application to emulate realtime solar data Apps, showing live and historical data from a solar panel <br><br>
Components needed: <br>
ESP8266 <br>
INA260 I2C 15A max voltage and current monitor <br> 
SSD1306 I2C OLED screen (optional) <br>
<br><br>
See this video for a demonstration of it working: <br>
https://www.youtube.com/watch?v=eLJJCFcRFXA
<br>
Update - The IP address of the connection is now shown on the SSD1306 screen and in the serial monitor  :)
<b>

The data is collected using an INA260 voltage/current sensor, passing the data over I2C to an ESP8266. Home WiFi credentials then allow that data to be displayed on a PC, tablet or phone. <br>
Data shown is the battery voltage, incoming current and wattage.
<br><br>
To install: <br>
Unzip the contents of the Zip file to your Sketch folder of the Arduino IDE. <br>
There will be a file called HomeSolarApp.ino and a data folder. Within the data folder is the HTML webpage which should be uploaded to SPIFFS using the Arduino IDE. The Arduino sketch contains an area for your home WiFi credentials to be entered. Edit those details to use the App. 
<br>
<br>
The App is based on code by Rui Santos of RandomNerdTutorials.com. Here is a similar full example project on that site: <br> 
https://randomnerdtutorials.com/esp32-esp8266-plot-chart-web-server/ <br>
SPIFFS is used to store the HTML webpage that the data is shown on and, using the tutorial above, you can learn how to upload data to the ESP8266 using SPIFFS. <br><r>
Circuit connections are only those for I2C, on a Wemos D1 R2 mini they are: <br>
D1 ---> SCL <br>
D2 ---> SDA <br>
<br>
Also, note the Ground connection from the solar panel needs to connect to the INA260's Ground connection for the INA260 to work.

