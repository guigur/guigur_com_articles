---
draft: true 
date: 2024-04-17
lang: en
categories:
  - Electronics
authors:
  - guigur
---

## Presentation
As of the beginning of this year, I worked as an intern at a small IoT company. 
The internship was quite short, and the founder of the company did not pay me because he was not legally obliged to do so. But he lent to me an old Keithley 175 multimeter. 
I was quite happy to have an old piece of kit in my army of lab equipment. But, there was a catch. This nice DMM has a broken screen. 
And worst of all, it’s the kind of screen with modes and units displayed on it. 
And as you may have guessed from the title of this project, the screen was unobtainium of course.
<!-- more -->

## Finding a replacement.

And so, my quest to repair this old and obsolete lab equipment began. 
I disassembled the unit and searched on the web for the part number of the original screen with no luck.

This search yielded the service manual of the Keithley 175.
This document is a real treasure. Schematics of the whole thing exploded view of all the mechanical assembly, and even code to remote control the device and perform the calibration.

## Replicating the screen layout

## Decoding the frame

I used a logic analyzer to decode the frame. At first, I was not sure what interface was used to control the LCD controller.
After some probing, and a lot of coffee, I was pretty convinced that bus was SPI.
I found on the interweb the datasheet of the LCD controller and at first tried to re-implement the behavior of his registers and commands.
But after some time, I deduced that I needed to see what the screen was supposed to display to decode this.
I searched mouser.com and found the _VIM-503-DP-RC-S-HV_* which had a similar pinout and the 3 commons pins like the Keithley 175 original display.
Without a second thought, I ordered this LCD and finally, I had some progress. 
With this screen, I can see 4 and a half digits and with the help of my digital analyzer make sense of the data.
I finally succeeded to decode the digits and options.

## The RAM problem

The lib I chossed, is the mighty u8g2 lib. This lib is great, it support lot of screens and a ton of fonts.
**BUT** it require a lot of RAM.
No problem, I used a ESP8266 to prototype the interface and the 2kB of RAM usage is not a problem anymore.

The Raspberry pico is the best microcontroller for the job
