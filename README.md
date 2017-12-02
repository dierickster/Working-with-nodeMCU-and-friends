# Working with nodeMCU and friends in the IoT era

## What to expect here? 

I will use this space for accumulating my experience with and thoughts about nodeMCU and its friends. Many of the items will be just *placeholders* for my personal sticky yellow notes and other volatile notes. Over time some may items may materialise into more mature features. 

If you have any additions or remarks, your input is welcome!

Code resides in the repository. Other documents live in the wiki: https://github.com/dierickster/Working-with-nodeMCU-and-friends/wiki


## Introduction 
Almost a revolution in the field of Domotics and related fields was started in the beginning of 2014 with the introduction of the ESP8266 device. This very cheap, poststamp sized *board* is able of doing Arduino-like things, and even has one more special trick up his sleeves.

Until then many enthusiastics around the globe used Arduino, while a few years later others switched to Raspberry Pi, for their home brewn automation tasks. Being a software and hardware developer myself, I was mesmerized by the possibilities of both platforms when I first got to know them. Before Arduino there already existed more technical, more expensive and less versatile hardware solutions, and they are still in active use and development. These kind of systems are out of scope of this repository. 

Although totally different in nature - both Arduino and Raspberry Pi systems have specific strong and weak points - they are pretty capable of doing many of the things you ever wanted to do with, or perhaps even did, with earlier predecessor systems  as mentioned before. 

Both Arduino and Raspberry Pi have what are called GPIO pins. GPIO stands for *General Input and Output pins* and gives us an interface for working with analog input and output (e.g. buttons and LED's), but also PWM and I2S. Many nice software libraries and additional hardware boards which interact with GPIO are available. IN the IoT dogma, the essential way of communicating with a more or less standalone device is wireless. For our purpose WiFi is de facto the standard, although e.g. GPS or LORA could be a good altenative. 

Arduino has several additional hardware extention boards which can be bought separately and communicate through the GPIO pins. Early Raspberry Pi's offered WiFi with the use of an additional USB device. Recent Pi's are available with WiFi incorporated.

As all ESP8266 devices come with onboard WiFi, and are hence IoT-ready. When introduced, this was and probably is a very unique property, considering price, speed of the device, footprint, power consumption and other aspects.

When I joined the ESP8266 bandwagon first, a few months after its introduction, communicating with it using its serial port protocal was not very easy. Several identical looking devices where shipped from China, with minor and major changes in both firmware and hardware. 

A major hurdle for getting an early ESP8266 board up and running, was that it is a true 3V3 device, which required some kind of voltage leveling when you want to program it with USB from a PC. After a while cheap programming interfaces arrived on the market. Additionally the Arduino community quickly brought us the possibility to program a ESP8266 as an Arduino sketch, where ESP8266 must be selected as the target board (mimicing an Arduino). 

Now the original family of cheap ESP8266 boards could be programmed with the use of an additional breakout board, while it would run its *sketch* afterwards without it. A drawback of the original family of cheap ESP8266 boards is that they offers only a few of the GPIO pins to the outside world, while much more are available internally. For most small hobby projects this is sufficient, but limiting for others. Programming a sketch in the Arduino *C*-like language is considered awkward by some due to its technical nature. 

With the introduction of *nodeMCU* and its associated development boards, some of the drawbacks were mitigated. Current development boards, which are commonly refered to as *nodeMCU*, piggyback the ESP32 board, which is a newer and more elaborated version of the original ESP8266 boards.  

Unlike the original board the nodeMCU can be used with a breadboard, and has the programming interface and USB connector integrated. Another change was that now the LUA programming language can be used. This is considered by some more natural as writing an Arduino sketch. This certainly may have helped to widen the audience from more or less *technically skilled* to *beginners* and the success of nodeMCU.

Being more costly than the ESP8266 board (about 4-5 times more expensive) the development board is still pretty cheap. The ESP32 board is firmly soldered onto the nodeMCU. Until now, I've never seen a true development board where the ESP32 can be interchanged, and after development and programming be put into the final target enviroment. 

Anyhow, it seems that nodeMCU or its friends are here to stay, and will partly become a part of the IoT reality around us! In my house its infiltration and replacement of traditional devices is already noticable.

So far this introduction, which I've written mostly for my own pleasure.




