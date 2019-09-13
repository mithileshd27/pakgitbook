---
oldwikiname: Grove_-_Serial_Camera
bzprodimageurl: 'http://statics3.seeedstudio.com/images/product/Serial Camera.jpg'
prodimagename: Serial_camera.jpg
surveyurl: 'https://www.research.net/r/Grove-Serial_Camera'
bzurl: 'https://seeedstudio.com/Grove-Serial-Camera-Kit-p-1608.html'
title: Grove - Serial Camera
tags: 'grove_uart, io_5v, plat_duino'
sku: 101020064
category: Others
---

# Grove Serial Camera

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/img/Serial_camera.jpg)

The Serial Camera is a JPEG color camera module easy for MCU use.It has integrated image processing DSP to generate 320_240 or 640_480 JPEG image without thumbnail information, Captured picture will be stored in internal buffer and transferred via UART port.

## Features

* Grove Interface
* JPEG compressed image without Thumbnail Information
* 5V power supply
* Small and compact
* Protocol control

## Specifications

|  Item |  Min |  Typical |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Operating Voltage |  4,8 |  5.0 |  5.3 |  V |
|  Resolution \(default\) |  640x480 / 320x240 |  / |  |  |
|  Default Baud rate of serial port |  115200 |  Baud |  |  |

## Platforms Supported

## Application Ideas

* Digital Cameras with the [SD card shield](http://www.seeedstudio.com/depot/sd-card-shield-p-492.html?cPath=109)
* Video monitoring system

## Usage

### Use Camera on PC

**Step 1**:Download dedicated serial port debugging tool [VC0703COMTOOL.rar](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/res/VC0703COMTOOL.rar) and install it.

**Step 2**: Connect Serial camera to PC with USB to use serial converter tool [UartSBee](/UartSBee_v5)

| Serial camera | Uart\_SB v3.1 |
| :--- | :--- |
| GND \(black\) | GND |
| VCC \(red\) | VCC |
| RX \(white\) | TX |
| TX \(Yellow\) | RX |

**Step 3:** Connect the Uart\_SB v3.1 with Computer and Open the vc0703CommTool software. Choose the correct COM number of the port you link to the camera, default baudrate 115200 ,and then open the port.

**Step 4:** Click the button "Get Version" and it will reset the camera.

**Step 5:** Click the button "Fbuf" to get ready to take a picture.

1. Click "stop CFbuf" to take a picture.
2. Click "Sel File" to select the file name to store the picture.
3. Click "Read" to read the data from the buffer to store in the file selected as shown below:

   ![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/img/Serial_Camera_Picture.jpg)

4. Click "Resume" to resume frame update so you can continue to take another picture.

### Use Camera with Arduino and SD card

**Step 1**: Connected Grove - Serial Camera to Arduino board, Hardware parts include [Seeeduino V3.0](http://www.seeedstudio.com/depot/seeeduino-v30-atmega-328p-p-669.html?cPath=132_133), [SD Card Shield](http://www.seeedstudio.com/depot/sd-card-shield-p-492.html?cPath=109), SanDisk microSD™ Card 2GB, [Grove - Button](http://www.seeedstudio.com/depot/grove-button-p-766.html?cPath=156_160).

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/img/Serial_Camera.jpg)

**Step 2**: Change the serial receive buffer\(default 64 bytes\) to 128 bytes. Open up hardware/arduino/cores directory, and edit the file named wiring\_serial.c or HardwareSerial.cpp near the top is a \#define SERIAL\_BUFFER\_SIZE 64, which means 64 bytes are used for the buffer. You need to change this to 128 .More details, please refer to [Arduino Hacks](http://learn.adafruit.com/arduino-tips-tricks-and-techniques/arduino-hacks).

**Step 3**: Download the [Grove - Serial Camera Library](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/res/SerialCameral_DemoCode.zip), upload it to Seeeduino. If it can't be complied, please confirm if the [SD Library](http://arduino.cc/en/Reference/SD) is in your Arduino IDE folder.

**Step 4**: Open the Serial Monitor , press the button to take picture after SD card and Camera initialization.

## Resources

* [VC0703 debug tool](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/res/VC0703COMTOOL.rar)
* [Manual for serial camera.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/res/Manual_for_serial_camera.pdf)
* [Grove - Serial Camera Library](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial_Camera/master/res/SerialCameral_DemoCode.zip)

