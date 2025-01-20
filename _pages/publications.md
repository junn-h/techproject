---
layout: archive
title: "About"
permalink: /Security Camera Project/
author_profile: true
---

I decided to try to create a security camera system which would be activated manually, or if it was nighttime and motion was detected. When activated, it would send a notification to my phone, and a picture would be able to be saved. However, I faced some challenges and I was ultimately not able to successfully complete this project.

### Circuit
The first step was to create a circuit for the camera. I made a circuit with a pir motion sensor, a photoresistor, transistors, an AND gate, an OR gate, a slideswitch and an LED for testing. The circuit will will light an LED if the motion sensor and the photoresistor output a high signal, or if the switch was turned on manually. The circuit worked with the LED, and it confirmed that I would only need to program the actual camera to get it working.![breadboard](https://raw.githubusercontent.com/junn-h/techproject/refs/heads/master/images/breadboard.jpg)

### Programming ESP32
I used an ESP32 for its low cost as the camera. I used an FTDI mini USB to TTL serial converter adapter to connect it into my PC. I used Arduino IDE to program the camera. I ran into some difficulty flashing the code, but after using different jumper cables, I was able to fix it. ![ftdi](https://raw.githubusercontent.com/junn-h/techproject/refs/heads/master/images/ftdi.jpg) The plan was to upload photos taken by the camera to an app called Blynk, where I would recieve a notification if the camera was alerted, and I could also take a picture manually. However, the camera would flash periodically without any way to control it. The serial monitor came back with errors, so I decided to try a different FTDI adapter and a different USB cable. ![error1](https://raw.githubusercontent.com/junn-h/techproject/refs/heads/master/images/error.PNG) This did not prove successful, so I decided to try different code. This new code has the same functionality, but it would instead upload photos to Telegram, however the serial monitor still came back with errors. ![error2](https://raw.githubusercontent.com/junn-h/techproject/refs/heads/master/images/error2.PNG) These errors indicated that the camera itself was most likely faulty. I tried using different versions of Arduino IDE, jumper cables, FTDI adapters, USB cables, and a different PC. Ultimately, I could not find a solution to my problem, and there is a high likelihood that I was either sent a faulty camera, or I had broken it. 
