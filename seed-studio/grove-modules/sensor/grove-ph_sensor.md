---
title: Grove - PH Sensor
category: Sensor
bzurl: 'https://www.seeedstudio.com/Grove-PH-Sensor-p-1564.html'
oldwikiname: Grove - PH Sensor
prodimagename: Phsensor.jpg
surveyurl: 'https://www.research.net/r/Grove_PH_Sensor'
sku: 101020065
---

# Grove PH Sensor

![](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/img/Phsensor.jpg)

Do you need to measure aqueous solution pH? Here, the Grove - PH sensor can help you do it. This sensor can output signal which corresponding to the hydrogen ion concentration that measured by PH electrode. Because it can be directly connected to controller,and then you can observe the PH value at any time. This device can be used for PH measurements, such as waste water, sewage and other occasions.

## Feature

* Grove Interface
* Wide measuring range
* Usage Life is two years
* Isopotential Point: pH 7.00 \(0 mV\)

## Specification

|  Item |  Typical |  Units |
| :--- | :--- | :--- |
|  Working Voltage |  5 |  V |
|  Isopotential point |  7±0.5 |  pH |
|  Measure Range |  0~14 |  pH |
|  pH Sensor Output Range |  -414.12 ~ 414.12 |  mV |
|  Measure Accuracy |  &lt;15 |  mV |
|  Response Time |  &lt;2 |  min |
|  Temperature Range |  0~60 |  ℃ |

## Schematic

![](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/img/PH_Sensor_Schematic.jpg)

## Usage

The pH sensor can help you to detect pH value. The success or failure of pH measurement depends on the PH sensor calibration and maintenance. Now let us get started from how to calibrate.

### Calibration

* Before using, you need using pure water or deionized water to wash it and then sop up the water with paper\(the paper is without hemp\). Remember,you'd better not wipe it because wiping PH electrode will cause errors. Here is a picture for reference:

  \*

  ![](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/img/PH_Sensor_Usage.jpg)

In this picture, PH 9.18 [buffer solution](http://www.chemguide.co.uk/physical/acidbaseeqia/buffers.html) is used as a reference solution, which helps us to know whether the measured value is accurate. Now let's look at what is the measured value.

* Upload the demo code. Please click [here](/Upload_Code) if you do not know how to upload

```text
//Function: The PH sensor output voltage value,
//          convert into PH and then display in the serial monitor.
#define Vref 4.95
void setup()
{
    Serial.begin(9600);
}
void loop()
{
    int sensorValue;
    int m;
    long sensorSum;
    for(m=0;m&lt;50;m++)
    {
        sensorValue=analogRead(A0);//Connect the PH Sensor to A0 port
        sensorSum += sensorValue;
    }
    sensorValue =   sensorSum/50;
    Serial.print(" the PH value is");
    Serial.println(7-1000*(sensorValue-372)*Vref/59.16/1023);

}
```

* Open the serial monitor for see the result:

![](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/img/PH_Sensor_result.jpg)

* Look at the result, you can see the test result is consistent with the actual value. So you can begin to measure aqueous solution pH. If there were errors between reference liquid PH and measured PH value, you had better soak the PH electrode for several hours and then recalibrate. [Here](http://www.ehow.com/how_4796148_calibrate-ph-meter.html) is a guide about how to calibrate for reference.

**Note:** If the measured value you get maintains higher or smaller than it should be, the reason could be a inappropriate Vref value. Vref is the working voltage of Arduino.

The relationship between PH value and the output voltage:

E=59.16\(mV/PH\)

### Cleaning and Storing

The pH electrode is the most sensitive component of your pH instrument. And the pH electrode cannot be allowed to dry out or freeze. The proper maintenance will provide years of reliable measurement. So [the pH electrode care and maintenance](http://www.eutechinst.com/techtips/tech-tips26.htm) is no less important than calibration. Please remember: when it’s not in use, you should wash and keep it in the 3mol Kcl container. The 3mol KCL need you to prepare. The preparation method can refer to the below information:

Based on 3 mol \* \( 74.55 g / 1 mol KCl\) = 223.65 g KCl So to prepare a 3 mol / L solution KCl, you'd need to dissolve 223.65 g of KCl into some water, mix, and then fill it up to the 1 L mark with water.

Hope this helps!

## Resource

* [Grove - PH Sensor Eagle File](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/res/Grove-PH_Sensor_Eagle_File.zip)
* [Grove - PH Sensor Schematic in PDF](https://github.com/SeeedDocument/Grove-PH_Sensor/raw/master/res/Grove-PH_Sensor_v1.0.pdf)

