# Home-Solar-App
A simple application to emulate realtime solar data Apps, showing live and historical data from a solar panel <br><br>
Components needed: <br>
ESP8266 <br>
INA260 I2C voltage and current monitor <br> 
SSD1306 I2C OLED screen (optional) <br>
<br><br>
The data is collected using an INA260 voltage/current sensor, passing the data over I2C to an ESP8266. Home WiFi credentials then allow that data to be displayed on a PC, tablet or phone. <br>
Data shown is the battery voltage, incoming current and wattage.
<br><br>
The App is based on code by Rui Santos of RandomNerdTutorials.com. Here is a similar full example project on that site: <br> 
https://randomnerdtutorials.com/esp32-esp8266-plot-chart-web-server/ <br>
SPIFFS is used to hold the HTML webpage that the data is shown on and, using the tutorial above, you can learn how to upload data to the ESP8266 using SPIFFS. <br><r>
Circuit connections are only those for I2C, on a Wemos D1 R2 mini they are: <br>
D1 ---> SCL <br>
D2 ---> SDA <br>
<br>
Aslo, note the Ground connection from the solar panel needs to connect to the INA260's Ground connection for the device to work.

The Arduino sketch contains an area for your home WiFi credentials to be entered. Edit those details to use the App :)
