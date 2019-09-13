---
oldwikiname: Grove_-_Magnetic_Switch
bzprodimageurl: 'http://statics3.seeedstudio.com/images/101020038 1.jpg'
prodimagename: Magnetic_Switch.jpg
surveyurl: 'https://www.research.net/r/Grove-Magnetic_Switch'
bzurl: 'https://seeedstudio.com/Grove-Magnetic-Switch-p-744.html'
title: Grove - Magnetic Switch
tags: 'grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_bbg, plat_wio'
sku: 101020038
category: Sensor
---

# Grove Magnetic Switch

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/Magnetic_Switch.jpg)

This is a Grove interface compatible Magnetic switch module. It is based on encapsulated dry reed switch CT10. CT10 is single-pole, single throw \(SPST\) type, having normally open ruthenium contacts. The sensor is a double-ended type and may be actuated with an electromagnet, a permanent magnet or a combination of both. The magnetic switch is a wonderful tool for designers who would like to turn a circuit on and off based on proximity.

## Features

* Grove compatible interface
* 2.0cm x 2.0cm Grove module
* Minimum external parts
* 10W rating
* Rugged encapsulation

## Application Ideas

* Proximity Sensor
* Security Alarm Sensor
* Level Sensor
* Flow Sensor
* Pulse Counter

## Specifications

|  Items |  Min |  Norm |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Working Voltage |  4.75 |  5.0 |  5.25 |  V |
|  Switched Power |  10 |  W |  |  |
|  Switched Voltage AC,RMS value\(max\) |  &lt; 140 |  V |  |  |
|  Switched Current DC |  &lt; 500 |  mA |  |  |
|  Carry Current DC |  &lt; 0.5 |  A |  |  |
|  Contact Resistance |  &lt;200 |  mΩ |  |  |
|  Insulation Resistance |  &gt;106 |  MΩ |  |  |
|  Operating Temperature |  -40 |  - |  125 |  ℃ |
|  Operate Range |  10 |  - |  40 |  AT |

## Platforms Supported

## Usage

### With [Arduino](/Arduino)

The SIG pin of the module output LOW normally. When a magnet approaches the switch, the magnetic switch close and the SIG pin output HIGH.

The following sketch demonstrates a simple application of using the Magnetic switch to control the led. When you put a magnet that has enough magnetic power close to the module, the switch is closed .Then the SIG pin out put a high voltage. You can use this to control the led.

As the picture on the below indicates, the Magnetic switch is connected to digital port 9 of the **Grove - Base Shield** and the LED is connected to digital port 13. When a Magnet approaches the switch, the SIG pin outputs a High voltage. Then the LED lights up. The hardware installation is as follows:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/Grove-Magnetic_Switch.jpg)

* Copy and paste code below to a new Arduino sketch.

```text
    /*******************************************************************************/

    /*macro definitions of magnetic pin and LED pin*/
    #define MAGNECTIC_SWITCH 9
    #define LED 13//the on board LED of the Arduino or Seeeduino

    void setup()
    {
        pinsInit();
    }

    void loop() 
    {
        if(isNearMagnet())//if the magnetic switch is near the magnet?
        {
            turnOnLED();
        }
        else
        {
            turnOffLED();
        }
    }
    void pinsInit()
    {
        pinMode(MAGNECTIC_SWITCH, INPUT);
        pinMode(LED,OUTPUT);
    }

    /*If the magnetic switch is near the magnet, it will return ture, */
    /*otherwise it will return false                                */
    boolean isNearMagnet()
    {
        int sensorValue = digitalRead(MAGNECTIC_SWITCH);
        if(sensorValue == HIGH)//if the sensor value is HIGH?
        {
            return true;//yes,return ture
        }
        else
        {
            return false;//no,return false
        }
    }
    void turnOnLED()
    {
        digitalWrite(LED,HIGH);
    }
    void turnOffLED()
    {
        digitalWrite(LED,LOW);
    }
```

* Upload the code.
* Then the LED light when there is Magnetic approaches the switch. Have a try!

### With Raspberry Pi

1.You should have a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](/GrovePiPlus).

3.Connection

* Plug the Magnet Switch to grovepi socket D3 by using a grove cable.

4.Navigate to the demos' directory:

```text
    cd yourpath/GrovePi/Software/Python/
```

* To see the code \(this demo has the same usage with tilt switch\)

  ```text
  nano grovepi_tilt_switch.py   # "Ctrl+x" to exit #
  ```

  ```text
  import time
  import grovepi

  # Connect the Grove Tilt Switch to digital port D3
  # SIG,NC,VCC,GND
  tilt_switch = 3

  grovepi.pinMode(tilt_switch,"INPUT")

  while True:
      try:
          print grovepi.digitalRead(tilt_switch)
          time.sleep(.5)

      except IOError:
          print "Error"
  ```

5.Run the demo.

```text
    sudo python grove_tilt_switch.py
```

6.Result

Put a magnet upon the sensor, the SIG pin will output HIGH.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/Grovepi_tilt_Switch_00.png)

## Resources

* [Grove-Magnetic Switch v0.9 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Magnetic_Switch.zip)
* [CT10 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/CT10.pdf)
* [Grove-Magnetic Switch v1.3 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_Eagle_File.zip)
* [Grove-Magnetic Switch v1.3 PDF File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_PDF_File.pdf)

