---
oldwikiname: Grove_-_2-Coil_Latching_Relay
bzprodimageurl: 'http://statics3.seeedstudio.com/images/product/2Coil Latching Relay.jpg'
prodimagename: 2Coil_Latching_Relay_01.jpg
surveyurl: 'https://www.research.net/r/Grove-2-Coil_Latching_Relay'
bzurl: 'https://seeedstudio.com/Grove-2-Coil-Latching-Relay-p-1446.html'
title: Grove - 2-Coil Latching Relay
tags: 'grove_digital, io_5v, plat_duino'
sku: 103020010
category: Actuator
---

# 2 Coil Latching Relay

![](https://raw.githubusercontent.com/SeeedDocument/Grove-2-Coil_Latching_Relay/master/img/2Coil_Latching_Relay_01.jpg)

This module is based on 2-Coil Latching Relay. Contrast to the ordinary relay, this latching relay does not need continuous power to keep the state, only a rising/falling pulse is needed to change the work state. Even the power can be removed when the work state do not need to change, making this module especially suitable for low-power projects.

## Features

* Grove Connector
* Low power consumption
* Dual Switch

## Specifications

|  Item |  Min |  Typical |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Working Voltage |  4.7 |  5.0 |  5.3 |  VDC |
|  Set/Reset Voltage\(Max\) |  4.0 |  VDC |  |  |
|  Coil Resistance |  151 |  167 |  183 |  Ω |
|  Switching Voltage\(Max\) |  35VAC/35VDC |  / |  |  |
|  Switching Current\(Max\) |  3 |  A |  |  |
|  Set Time\(Latching\) |  4.5\(max\) |  ms |  |  |
|  Reset Time\(Latching\) |  3.5\(max\) |  ms |  |  |

## Platforms Supported

## Before usage

### Related Reading

We suggest you to read those knowledge before using the Gas sensor, it'll help you to learn more about Arduino and our products, and also it'll let you to use open souse hardware more easier.

* [Getting Started with Arduino](/Getting_Started_with_Seeeduino)
* [What is Grove system](/Grove_System)
* [Why i need a Base shield?](/Base_Shield_V2)

After reading that you will know how to use Base shield with Grove products to work well with Arduino. Let's start it !

### To be prepared

This tutorial will include some necessary products:

* [Arduino UNO R3](http://www.seeedstudio.com/depot/Arduino-Uno-Rev3-p-694.html) or [Seeeduino v4](http://www.seeedstudio.com/depot/Seeeduino-V4-p-669.html)
* [Base Shield](http://www.seeedstudio.com/depot/Base-Shield-V2-p-1378.html)
* Grove - 2-Coil Latching Relay

## Getting Started

### With Arduino

The latching relay only draws power during the changing of state. A rising/falling voltage pulse on the signal pin changes it's working state. This is very useful in situations where energy efficiency is important, and also in situations where you need the relay to remember its state.

Let's begin to use it.

* Connect the module to D3 port of [Grove - Base Shield](/Base_Shield_V2).
* The relay hold in "set" status\(Comm and NO connected\) in default, when there is a rising edge on the SIG pin. It turns the "reset" state\(Comm and NC connected\). The reference code is shown below:

```c
#define LatchingRelay 3
void setup()
{
    pinMode(LatchingRelay,OUTPUT);

    digitalWrite(LatchingRelay,LOW);
    delay(1000);
    digitalWrite(LatchingRelay,HIGH);
    delay(1000);
}
void loop()
{

}
```

* The relay hold in "reset" status\(Comm and NC Connected\), when there is a falling edge on the SIG pin. It turns the "set" state\(Comm and NO connected\). The reference code is shown below:

```c
#define LatchingRelay 3
void setup()
{
    pinMode(LatchingRelay,OUTPUT);

    digitalWrite(3,HIGH);
    delay(1000);
    digitalWrite(3,LOW);
    delay(1000);
}
void loop()
{

}
```

* This module consumes little power when working state doesn't change. After setting the relay state, you do not need to supply power for the Latching Relay any more, which makes it especially low power consumption.

Note Relay is on the "reset" status when being released from stock.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-2-Coil_Latching_Relay/master/img/Latching_Relay_Diagram.jpg)

Notes

 1. The two-way relays are controlled at the same time.

 2. The NO\(NC\) indicator will flash once when switch to "set"\("reset"\) status.

### With Raspberry Pi

1.You should have got a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](/GrovePiPlus).

3.Connection

* Plug the sensor to grovepi socket D4 by using a grove cable.

4.Navigate to the demos' directory:

```text
cd yourpath/GrovePi/Software/Python/
```

* To see the code

```text
nano grove_2_coil_latching_relay.py   # "Ctrl+x" to exit #
```

```text
import time
import grovepi

# Connect the Grove 2-Coil Latching Relay to digital port D4
# SIG,NC,VCC,GND
relay = 4

grovepi.pinMode(relay,"OUTPUT")

while True:
    try:
        # switch on for 5 seconds
        grovepi.digitalWrite(relay,1)
        print "on"
        time.sleep(5)

        # switch off for 5 seconds
        grovepi.digitalWrite(relay,0)
        print "off"
        time.sleep(5)

    except KeyboardInterrupt:
        grovepi.digitalWrite(relay,0)
        break
    except IOError:
        print "Error"
```

5.Run the demo.

```text
sudo python grove_2_coil_latching_relay.py
```

## Resources

* [Grove - 2-Coil Latching Relay Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-2-Coil_Latching_Relay/master/res/Grove-2-Coil_Latching_Relay_Eagle_File.zip)
* [Latching\_Relay\_Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-2-Coil_Latching_Relay/master/res/Latching_Relay_Datesheet.pdf)

