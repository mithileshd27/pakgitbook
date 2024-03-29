---
oldwikiname: Grove_-_LED_Matrix_Driver_v1.0
bzprodimageurl: 'http://statics3.seeedstudio.com/seeed/img/2016-07/POVQFNSv9hKluouORsqs2H5s.jpg'
prodimagename: Grove-LED_Matrix_Driver_v1.0_product_view_700_s.jpg
surveyurl: 'https://www.research.net/r/Grove-LED_Matrix_Driver_v1_0'
bzurl: 'https://seeedstudio.com/Grove-LED-Matrix-Driver-v1.0-p-2645.html'
title: Grove - LED Matrix Driver v1.0
tags: 'plat_duino, plat_pi, plat_bbg, plat_linkit'
sku: 105020013
category: Actuator
---

# Grove LED Matrix Driver

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/img/Grove-LED_Matrix_Driver_v1.0_product_view_700_s.jpg)

Grove - LED Matrix Driver v1.0 is UART \(Serial\) to dot matrix LED driver that incorporates various graphics functions.It can only support 32×64 LED matrix. This product is a **Grove** compatible UART interface. It provides easy and rich APIs that abstract the complexity of the underlying LED driving hardware. All you need to is just call these APIs in code to implement different functionalities for your project.

Each dot\(i.e pixel\) support dual color LEDs. It can produce three colors totally: red \(primary color\), green\(primary color\) and yellow \(mixed color\). The input current for all LEDs can be set at a time.

Note This Grove module does not support changing the input current of each LED separately.

## Features

* Grove compatible and easy to use
* Highly abstracted and complete API
* Support dual-color LED-pixel. Three colors totally \(the third color is a mix of two primary color\)
* Interface: UART\(SoftSerial in Arduino\)

## Specifications

| Parameter | Value |
| :--- | :--- |
| Operating voltage\(V\) | 3.3–5 Volts |
| Operating current\(mA\) | Maximum: 28–50 mA |
| Output voltage \(from matrix driver\) | 3.3 Volts |
| Symbols/Graphics functions supported | Dot, straight line, circle, char, string, number, emoji, image \(you can display these symbols by calling API directly in code\) |
| Supported LED matrix size | 32\(row\)×64\(column\) |
| Supported color in each LED matrix dot | Dual LEDs \(green and red\) and a mixed color\(yellow\), and you can use only one LED in each LED matrix dot |
| Connector for LED matrix | DBSTAR\_HUB 08A |
| Protocol for Grove port | UART |
| Working temperature | -40–80 ℃ |
| Dimensions | 46.5×44 mm |
| Weight | 9 g\(for the module\), 12.5\(for all single package\) |

## Platforms Supported

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/img/Grove-LED_Matrix_Driver_v1.0_product_components_described_1200_s.jpg)

* **Grove socket**, to connect this product to main control board.
* **LED matrix port\(DBSTAR\_HUB 08A \)**, to connect LED matrix. If you can not find a connector like this, you can user jumper wires as an alternative.

### **Package includes**\(main parts\)

| Parts name | Quantity |
| :--- | :--- |
| Grove - LED Matrix Driver v1.0 | 1 piece |
| [Grove cable](http://www.seeedstudio.com/depot/Grove-Universal-4-Pin-Buckled-5cm-Cable-5-PCs-Pack-p-925.html?cPath=98_106_57) | 1 piece |

## Getting Started

Now let us run some basic examples with this module.

### With Arduino

#### Material required

* Grove - LED Matrix Driver v1.0 × 1
* 32×64 LED matrix with one red and one green LEDs in matrix dots \(single color LED matrix will also be fine\) × 1
* Power line \(ribbon shape\) for × 1
* 5 Volts\(output\) Adapter to regulate input voltage for LED matrix × 1
* 8-pin\(female\) ribbon cable × 1
* Arduino UNO \(other Arduino models will also be fine\) × 1
* [Grove cable](http://www.seeedstudio.com/depot/Grove-Universal-4-Pin-Buckled-5cm-Cable-5-PCs-Pack-p-925.html?cPath=98_106_57) × 1
* Grove - Base Shield × 1

#### Connections

Connect all parts as following:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/img/Grove-LED_Matrix_Driver_v1.0_wiki_demo_connections_front_3600.jpg)

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/img/Grove-LED_Matrix_Driver_v1.0_wiki_demo_connections_back_3600.jpg)

#### Coding Work

You can find more demo sketch at [https://github.com/Seeed-Studio/Grove\_LED\_Matrix\_Driver](https://github.com/Seeed-Studio/Grove_LED_Matrix_Driver) and development library at [https://github.com/Seeed-Studio/Grove\_LED\_Matrix\_Driver/tree/master/Arduino/LEDMatrix](https://github.com/Seeed-Studio/Grove_LED_Matrix_Driver/tree/master/Arduino/LEDMatrix)

1. A typical demo code. You can upload code to main control board with [Codebender](https://codebender.cc).
2. Download and upload the code. If you do not know how to upload an Arduino sketch, please visit [https://www.arduino.cc/en/Guide/Windows](https://www.arduino.cc/en/Guide/Windows) for Windows user or [https://www.arduino.cc/en/Guide/MacOSX](https://www.arduino.cc/en/Guide/MacOSX) for Mac user. You can see the result as below.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/img/Grove-LED_Matrix_Driver_v1.0_wiki_demo_result_view_s.jpg)

## Resources

* [Schematic file](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/res/Grove_LED_Matrix_Driver_v1.0_Schematics.zip)
* [STM32F103C8T6 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Matrix_Driver_v1.0/master/res/STM32F03C8T6.pdf)
* [Library on Github](https://github.com/Seeed-Studio/Grove_LED_Matrix_Driver)
* [Firmware for this product](https://github.com/Seeed-Studio/Grove_LED_Matrix_Driver/tree/master/Firmware)

