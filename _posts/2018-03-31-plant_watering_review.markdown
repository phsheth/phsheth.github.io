---
layout: post
title:  "Plant Watering Project - the story Last Year"
excerpt: "A critical review of my plant watering project"
date:   2018-03-31 12:17:00 +0530
categories: blog
tag: python, scipy
---




So - its almost April and I have a long weekend to take a stock of things. One this I remember is the Plant Watering Project. I had named it WatrrBot.

Last year, 2017, I decided to make a circuit that could be used to periodically water plant pots in the balcony of my house.

The circuit design went well and following were the components I learnt and programmed:

1. Arduino Pro Mini 5v: works just like the Arduino Uno, only much more compact. Was using two of them - one as a master and second one as a slave. The master did the jobs of controlling the LCD display, accepting user input from the rotary encoder and reading time from the RTC.
2. LM7805 Buck Converter: This was the part that messed it up - more about that later.
3. Rotary Encoder: Worked like a charm -  although initial programming was a bit time consuming - but once I cracked how to code it - things were breeze.
4. 16x2 LCD Screen: Nice screen with blue led backlight - this may have been another culprit but I still doubt the LM7805 Buck Converter.
5. DS3231 RTC: No complaints here - worked like a charm with the correct library.

![initial_circuit](/img/blog/vid-20180330-wa0014.gif)

So - the above video shows the LM7805 buck converter that I ordered from a local vendor on ebay.in. But - after a few days of working - the converter burnt both my Arduino boards.

Otherwise - the assembly worked really well on the breadboard and looked like an early stage prototype of any gadget:

![initial_prototype](/img/blog/img_20170609_183408.jpg)

So - why I write this blog post? Since this failure - I have understood that I had made a mistake somewhere in selecting the stepdown of the power supply. So I did three courses on Coursera.org:

1. Introduction to Electronics - Georgia Tech
2. Introduction to Power Electronics - Uni of Colorado - Boulder
3. Converter Circuits - Uni of Colorado - Boulder

And now - I have a slightly better understanding of step down converters and which one to select for my project.

Starting today - I put a renewed effort in making this circuit - lets see how far it goes this time. This time:

1. The LM7805 is replaced by a compact buck converter that can convert 1 to 24 volts to 0.8 to 12 volts. Another change is - instead of the 16x2 LCD - I will use a 0.96'' OLED display (ordered from Aliexpress - should be here in a month).
2. Instead of using two boards (master and slave) - I can use a single board and use RTOS to perform the many tasks. We will have to plan this.
3. Instead of the gadget being continuously powered by a wall power supply - I can inclue 4 18650 batteries in it so that charging can be done only when required. This will involve learning and developing an inhouse battery management system for a 4S configuration.

Plan for the perfboard:

![perfboard_schematic](/img/blog/perfcb_planning_30mar18.png)

![perfboard_schematic_photo](/img/blog/img_20180330_235334.jpg)

Update: I uploaded the code to an arduino uno with all the connections, following are the observations:

1. the rotary encoder does work - but the response is very sporadic and inconsistent. Need to relook at how the encoder is put to work. Also check how to make it work within RTOS
2. The 16x2 LCD also behaves sporadic - might have to move to an OLED (parts already ordered)
3. Need to figure why this instability.
