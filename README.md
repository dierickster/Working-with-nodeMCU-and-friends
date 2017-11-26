# Working with nodeMCU and friends in the IoT era

## Introduction 
Almost a revolution in the field of Domotics and related fields was started in late 2014 with the introduction of the ESP8266 device. This very cheap, poststamp sized *board* is able of doing Arduino-like things, and even has one more special trick up his sleeves.

Until then many enthusiastics around the globe used Arduino at first, and a few years later some switched to Raspberry Pi, for their home brewn automation tasks. Being a software and hardware developer myself, I was mesmerized by the possibilities of both platforms when I first got to know them. Before Arduino more technical, more expensive and less versatile hardware solutions already were in use, and still are. These are out of scope of this repository. 

Although totally different in nature - both systems have specific strong and weak points - they are pretty capable of doing many of the things you ever wanted to do with, or perhaps even did, with earlier predecessor systems. 

Both Arduino and Raspberry Pi have what are called GPIO pins. GPIO stands for *General Input and Output pins* and gives us an interface for working with analog input and output (e.g. buttons and LED's), but also PWM and I2S. Many nice software libraries and additional hardware boards which interact with GPIO are available. An essential way of communicating with a more or less standalone device is WiFi. Arduino has several additional hardware *HAT*s for that purpose which can be bought separately and communicate through the GPIO pins. Early Raspberry Pi's offered WiFi with the use of an additional USB device. Recent Pi's are available with WiFi incorporated.

As all ESP8266 devices come with onboard WiFi this was and probably is a very unique property, considering price, speed of the device, footprint and other aspects.

When I joined the ESP8266 bandwagon first, a few months after its introduction, communicating with it still was not easy. Several identical looking devices where shipped from China, with minor and major changes in both firmware and hardware. 

At first a major hurdle was that it is a true 3V3 device, which required some kind of voltage leveling device when you want to program it with USB from a PC. After a while cheap programming interfaces arrived. Additionally the Arduino community quickly brought us the possibility to program a ESP8266 with an Arduino sketch, where ESP8266 must be selected as the target board (mimicing an Arduino). 

Now the original family of cheap ESP8266 boards could be programmed very easily with the use of an additional breakout board, while it runs it *sketch* afterwards without it. A drawback of the original family of cheap ESP8266 boards is that they offers only a few of the GPIO pins to the outside world, while much more are available internally. For most small hobby projects this will be sufficient, but limiting for others. Programming a sketch in the Arduino *C*-like language is considered awkward by some due to its technical nature. 

With the introduction of *nodeMCU* and its associated development boards, some of the drawbacks were mitigated. Current development boards, which are commonly refered to as *nodeMCU*, piggyback the ESP32 board, which is a newer and more elaborated version of the original ESP8266 boards.  

Unlike the original board the nodeMCU can be used with a breadboard, and has the programming interface and USB connector integrated. Being more costly than the ESP8266 board (about 4-5 times more expensive) the development board is still pretty cheap. The ESP32 board is firmly soldered onto the nodeMCU. Until now, I've not seen a true development board where the ESP32 can be interchanged and after development and programmed put into the final target enviroment. 












