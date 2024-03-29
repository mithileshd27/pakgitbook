---
oldwikiname: Grove_-_I2C_Color_Sensor
bzprodimageurl: 'http://statics3.seeedstudio.com/images/101020041 1.jpg'
prodimagename: Grove-I2C-Color-Sensor.jpg
surveyurl: 'https://www.research.net/r/Grove-I2C_Color_Sensor'
bzurl: 'https://seeedstudio.com/Grove-I2C-Color-Sensor-p-854.html'
title: Grove - I2C Color Sensor
tags: 'grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit'
sku: 101020041
category: Sensor
---

# Grove I2C Color Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/img/Grove-I2C-Color-Sensor.jpg)

This module is based on the color sensor TCS3414CS with digital output I2C. Based on the 8\*2 array of filtered photodiodes and 16-bit analog-to-digital converters, you can measure the color chromaticity of ambient light or the color of objects. Of the 16 photodiodes, 4 have red filters, 4 have green filters, 4 have blue filters and 4 have no filter\(clear\). With the synchronization input pin, an external pulsed light source can provide precise synchronous conversion control.

!!!Note Please note that the latest version V2.0 has replaced the IC with TCS3472 and the old library has also been updated, If you are using the V2.0 version, please use the [new library](https://github.com/Seeed-Studio/Grove_I2C_Color_Sensor_TCS3472).

## Features

* Grove compatible interface
* 16-Bit digital output with I2C
* SYNC Input Synchronizes Integration Cycle to Modulated Light Sources
* Operating temperature range -40°C to 85°C
* Programmable interrupt function with User-Defined Upper and lower threshold settings
* RoHS Compliant

## Specifications

| Parameter | Value/Range |
| :--- | :--- |
| PCB Size | 2.0 cm \* 4.0 cm |
| Interface | 2.0mm pitch pin header |
| VCC | 3.3 - 6.0 V |
| I2C Speed | 400 kHz |

## Platforms Supported

## Getting Started

Following documents help in getting the user started with Grove.

* [Preface - Getting Started](http://www.seeedstudio.com/document/pdf/Preface.pdf)
* [to Grove](http://www.seeedstudio.com/document/pdf/Introduction%20to%20Grove.pdf)

### Hardware Connections

Grove products have an eco system and all have the same connector which can plug onto the [Grove Base Shield](/Base_Shield_V2). Connect this module to the I2C port of Base Shield. However, you can also connect Grove - I2C Color Sensor to Arduino without Base Shield by jumper wires.

| Arduino UNO | Grove - I2C Color Sensor |
| :--- | :--- |
| 5V | VCC |
| GND | GND |
| SDA | SDA |
| SCL | SCL |

## Software Installation

[Download Arduino and install Arduino driver](/Download_Arduino_and_install_Arduino_driver)

[Getting Started with Seeeduino/Arduino](/Getting_Started_with_Seeeduino)

## Demos

This module can be used to detect the color of light source or the color of objects. When used to detect the color of the light source, the led switch should be turned off, and the light source should shine the sensor directly. When used to detect the color of things, the led should be on and you should put the object on the top of the enclosure closely. The theory of sensing the color of objects is Reflective Sensing Theory. Like the picture below.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/img/Reflcect.jpg)

### Color Sensor Library

We have created a library to help you start playing quickly with the Seeeduino/Arduino, in this section we'll show you how to set up the library.

#### Setup

1. Download the [library code as a zip file](https://github.com/Seeed-Studio/Grove_I2C_Color_Sensor) from the Grove\_I2C\_Color\_Sensor github page. If you are using the latest version V2.0\(IC is TCS3472 \), please use this [new library](https://github.com/Seeed-Studio/Grove_I2C_Color_Sensor_TCS3472)
2. Unzip the downloaded file into your …/arduino/libraries.
3. Rename the unzipped folder "Color\_Sensor"
4. Start the Arduino IDE \(or restart if it is open\).

#### Description of function

This is the most important/useful function in the library, we invite you to look at the .h and .cpp files yourself to see all the functions available.

**Read RGB data through the library function**

**readRGB\(int \*red, int \*green, int \*blue\)**

* **red:** The variable address to save R.
* **green:** The variable address to save G.
* **blue:** The variable address to save B.

```text
void loop()
{
    int red, green, blue;
    GroveColorSensor colorSensor;
    colorSensor.ledStatus = 1;            // When turn on the color sensor LED, ledStatus = 1; When turn off the color sensor LED, ledStatus = 0.
    while(1)
    {
        colorSensor.readRGB(&red, &green, &blue);    //Read RGB values to variables.
        delay(300);
        Serial.print("The RGB value are: RGB( ");
        Serial.print(red,DEC);
        Serial.print(", ");
        Serial.print(green,DEC);
        Serial.print(", ");
        Serial.print(blue,DEC);
        Serial.println(" )");
        colorSensor.clearInterrupt();
    }
}
```

### Color Sensor Examples/Applications

This example shows how to use features of Grove - I2C Color Sensor and display the detected color with a [Chainable RGB LED Grove](/Grove-Chainable_RGB_LED).

Note If you haven't downloaded [Grove-Chainable RGB LED library](https://github.com/Seeed-Studio/Grove_Chainable_RGB_LED) to your Arduino IDE before, please download and set up the library first.

* Open File-&gt;Examples-&gt;Color\_Sensor-&gt;example-&gt;ColorSensorWithRGB-LED sketch for a complete example, or copy and paste code below to a new Arduino sketch.

**Description**: This example can measure the color chromaticity of ambient light or the color of objects, and via Chainable RGB LED Grove, display the detected color.

You also can use other display modules to display the detected color by Grove - I2C Color Sensor.

```text
#include <Wire.h>
#include <GroveColorSensor.h>
#include <ChainableLED.h>

#define CLK_PIN   7
#define DATA_PIN  8
#define NUM_LEDS  1            //The number of Chainable RGB LED

ChainableLED leds(CLK_PIN, DATA_PIN, NUM_LEDS);

void setup()
{
    Serial.begin(9600);
    Wire.begin();
}

void loop()
{
    int red, green, blue;
    GroveColorSensor colorSensor;
    colorSensor.ledStatus = 1;            // When turn on the color sensor LED, ledStatus = 1; When turn off the color sensor LED, ledStatus = 0.
    while(1)
    {
        colorSensor.readRGB(&red, &green, &blue);    //Read RGB values to variables.
        delay(300);
        Serial.print("The RGB value are: RGB( ");
        Serial.print(red,DEC);
        Serial.print(", ");
        Serial.print(green,DEC);
        Serial.print(", ");
        Serial.print(blue,DEC);
        Serial.println(" )");
        colorSensor.clearInterrupt();
        for(int i = 0; i<NUM_LEDS; i++)
        {
            leds.setColorRGB(i, red, green, blue);
        }
    }
}
```

* Upload the code to the development board.
* Then Grove\_-\_Chainable\_RGB\_LED would display the color which is detected.

## Other Reference

This module is based on the color sensor TCS3414CS. The TCS3414CS digital color sensor returns data from four channels: red\(R\), green\(G\), blue\(B\) and clear\(C\)\(non-filtered\). The response from the red, green and blue channels \(RGB\) can be used to determine a particular source’s chromaticity coordinates \(x, y\). These standards are set by the Commission Internationale de l’Eclairage \(CIE\). The CIE is the main international organization concerned with color and color measurement.In order to acquire the color of a given object using TCS3414CS, we must first map the sensor response \(RGB\) to the CIE tristimulus values \(XYZ\). It is then necessary to calculate the chromaticity coordinates \(x, y\).

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/img/Coordinates_transform.png)

Chromaticity Calculation Process Overview

The equations to do the transformation:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/img/Equations.png)

Transformation Equations

* When we get coordinates \(x, y\), please reference the below figure so as to get the recommended color.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/img/Chromaticity_Diagram.jpg)

## Resources

* **\[Library\]**[Library for Grove - I2C Color Sensor V1.2](https://github.com/Seeed-Studio/Grove_I2C_Color_Sensor)
* **\[Library\]**[Library for Grove - I2C Color Sensor V2.0](https://github.com/Seeed-Studio/Grove_I2C_Color_Sensor_TCS3472)
* **\[Eagle\]**[Grove-I2C Color Sensor Eagle File V1.2](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove-I2C%20Color%20Sensor%20Eagle%20File%20V1.2.zip)
* **\[Eagle\]**[Grove-I2C Color Sensor Eagle File V2.0](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove%20I2C%20Color%20Sensor%20v2.0.zip)
* **\[PDF\]**[Grove-I2C Color Sensor SCH File V1.2](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove%20-%20I2C%20Color%20sensor%20v1.2%20SCH.pdf)
* **\[PDF\]**[Grove-I2C Color Sensor SCH File V2.0](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove%20-%20I2C%20Color%20sensor%20v2.0%20SCH.pdf)
* **\[PDF\]**[Grove-I2C Color Sensor PCB File V1.2](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove%20-%20I2C%20Color%20sensor%20v1.2%20PCB.pdf)
* **\[PDF\]**[Grove-I2C Color Sensor PCB File V2.0](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/Grove%20-%20I2C%20Color%20sensor%20v2.0%20PCB.pdf)
* **\[Datasheet\]**[TCS3414-A Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-I2C_Color_Sensor/master/res/TCS3404_TCS3414-A.pdf)
* **\[Datasheet\]**[TCS3472 Datasheet](https://github.com/SeeedDocument/Grove-I2C_Color_Sensor/raw/master/res/TCS3472%20Datasheet.pdf)



