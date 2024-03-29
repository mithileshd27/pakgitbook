---
oldwikiname: Grove_-_I2C_Touch_Sensor
bzprodimageurl: 'http://statics3.seeedstudio.com/images/P3202380.jpg'
prodimagename: Grove-I2C-Touch-Sensor.jpg
surveyurl: 'https://www.research.net/r/Grove-I2C_Touch_Sensor'
bzurl: 'https://seeedstudio.com/Grove-I2C-Touch-Sensor-p-840.html'
title: Grove - I2C Touch Sensor
tags: 'grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit'
sku: 101020047
category: Sensor
---

# Grove I2C Touch Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/img/Grove-I2C-Touch-Sensor.jpg)

The I2C Touch Sensor is based on the Proximity Capacitive Touch Sensor Controller from FreeScale - MPR121. It detects the touch or proximity of human fingers. This sensor includes a Touch Sensor controller and 4 finger feelers. One can insert the connectors of feelers into base of Sensor controller, and start sensing the touch.

## Specifications

| Parameter | Value/Range |
| :--- | :--- |
| Operating voltage | 3~5.5V |
| Standby Mode Current | 2μA |
| Touch Channels | 12 \(Including 4 with Touch feelers\) |
| Communicating Protocol | I2C |
| I2C Address | 0x5A - 0x5D |

## Platforms Supported

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/img/DSC_0030.png)

There are 12 electrodes CH0-CH11. CH0-CH3 are connected to 4 Touch feelers.

The CH4-CH11 are for customer expanding the function. If you need more, you can make the feelers by yourself.

The wires of feelers are twisted to reduce the impact of environment. The black\(ground\) wire can be cut off if high sensitivity is needed.

The INT pin has to be led out if customers want to use the interrupt pin of MPR121.

## Getting Started

### **Grove - Help**

Following documents help in getting the user started with Grove.

* [Preface - Getting Started](http://www.seeedstudio.com/document/pdf/Preface.pdf)
* [to Grove](http://www.seeedstudio.com/document/pdf/Introduction%20to%20Grove.pdf)

Note Since each electrode needs to be auto-configured by the MPR121 during power up and there is no power reset on the touch sensor controller, everytime you insert or remove a feeler, you need to reset the power of Seeeduino.

The feelers can also feel the human being fingers with something between, that's to say, you do not need to touch the feelers with your fingers indeed.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/img/DSC_0026.jpg)

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/img/DSC_0027.jpg)

With a paperboard about 3 mm thick, the feeler can feel the touch of fingers, makes it a good solution for many applications.

## Resources

* [I2C Touch Sensor Library](https://github.com/Seeed-Studio/Grove_I2C_Touch_Sensor)
* [I2C Touch Sensor eagle files\(v1.1\).zip](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/res/I2C_Touch_Sensor_eagle_files-v1.1-.zip)
* [I2C Touch Sensor PDF](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/res/Grove-I2C_Color_sensor_v1.2.pdf)
* [How to detect finger touch?](/How_to_detect_finger_touch?)
* [I2C Touch Sensor Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Touch_Sensor/master/res/Freescale_Semiconductor;MPR121QR2.pdf)

