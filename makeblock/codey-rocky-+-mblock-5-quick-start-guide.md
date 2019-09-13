# Codey Rocky + Mblock 5 Quick Start Guide

![](../.gitbook/assets/0%20%2814%29.png)

\*\*\*\*

![ ](../.gitbook/assets/1%20%282%29.png)

For the latest version, please go to the following website:

[http://www.mblock.cc/software/mblock/mblock5/](http://www.mblock.cc/software/mblock/mblock5/)

**Interface and Glossary**

![](../.gitbook/assets/2%20%288%29.png)

Blocks Area ，Scripts Area，Stage Area

* Blocks Area: An area where blocks available for programming are provided. You can find any blocks that you need by category and color.
* Scripts Area: An area where blocks can be dragged here to write programs.
* Stage Area: In this area, you can display your works, connect the device, upload to the device, add sprites and backgrounds, etc.

**Examples Programs**

![codey](../.gitbook/assets/3%20%2814%29.png) ![codey](../.gitbook/assets/4%20%288%29.png)

Alpha.8 has 12 new examples programs. Some of the projects in this document can be found in Examples Programs as well.

**Connect Device**

First, power on your codey. Next, connect the codey with a computer via the USB cable or the Bluetooth adapter.

* Start the software mblock. Click Connect Device.

![](../.gitbook/assets/5%20%2814%29.png)

* Click Connect.

![](../.gitbook/assets/6%20%284%29.png)

Note: The COM3 here refers to the serial port number and it might vary from different systems and computers. Anyway, you can just click Connect.

**1. Start with your First Project** _**（Beginner）**_

* Drag an Events Block to the Scripts Area.

![](../.gitbook/assets/7%20%282%29.png)

* Add a Sound Block and select a sound effect.

![](../.gitbook/assets/8%20%285%29.png)

* Click Upload to Device.

![](../.gitbook/assets/9%20%286%29.png)

Press the Button A on codey and you will hear some sounds from codey.

* Add the image block. You can choose the image by default, or you can draw up an image you like with your mouse.

![](../.gitbook/assets/10%20%281%29.png)

![](../.gitbook/assets/11%20%284%29.png)

* Let’s draw up more images and control them with Button A, B, C.

![](../.gitbook/assets/12%20%286%29.png)

Tip: You can right-click the blocks to duplicate the scripts and right-click in the blank Scripts Area to rearrange all the blocks.

![codey](../.gitbook/assets/13%20%282%29.png) ![codey](../.gitbook/assets/14.png)

1. Upload the program to device and save the program. ![codey](../.gitbook/assets/15%20%284%29.png)
2. Last step! Show your project to friends and families!

**2.Make an Animation: Joggle Bouncy Balls** _**（Beginner）**_

In this project, you will learn how to make an animation with codey and how to trigger it in a funny way:

* The following block is needed in this project:

![](../.gitbook/assets/16%20%281%29.png)

* Open a New File. Then, draw a floppy ball. Make it just look like lie on the floor.

![](../.gitbook/assets/17.png)

* Keep on. Now, draw a ball that bounces up. Then, snap together this block and the former one, and set time to 0.3 sec.

![](../.gitbook/assets/18.png)

![](../.gitbook/assets/19%20%282%29.png)

* Go on to finish the image. Draw up the entire process of bouncy ball from bouncing up to landing.

![](../.gitbook/assets/20.png)

* Add a sound and a trigger event.

![](../.gitbook/assets/21%20%281%29.png)

* Upload the program and shake codey. Now, what is happening?

By tying codey to your body, you can find that the bouncy ball will bounce up as you jump up.

Tips: 1. You can use different Events to trigger the animation. 2. You can change the animation speed by adjusting the time duration.

**3.Execute Simultaneously: Alarm** _**（Beginner）**_

A combination of the blocks can simply serves as a script. _**As for codey, it can execute six scripts at most simultaneously.**_。

This program includes two scripts. One script is designed to make codey repeat the sound and another script is to make codey flash on and off, on and off...

![](../.gitbook/assets/22.png)

Tip: You can add one more scripts to control volume of codey with the gear potentiometer.

![](../.gitbook/assets/23%20%281%29.png)

Note: You can find the gear potentiometer on the side of codey.

![](../.gitbook/assets/24%20%281%29.png)

**4.Images Coordinates** _**（Intermediate ）**_

* This demo uses the following blocks

![](../.gitbook/assets/25%20%281%29.png)

You can use this block to display the images at any specified coordinate positions. To get the accurate coordinate, please refer to the top left-corner of the image.

![](../.gitbook/assets/26%20%281%29.png)

Tip: Open the Image Editor. Just click on the icon “![codey](../.gitbook/assets/27%20%281%29.png) ” to show the coordinates.

* Try the following script and check how the program works.

![](../.gitbook/assets/28.png)

**5.Variable and Coordinate-Running Rabbit** _**（Advanced）**_

Thanks Ekime for drawing up the rabbit image for us and helping the writer finish this project.

The Variables function can enable the image to move:

* Create a Variable

![](../.gitbook/assets/29.png)

In mblock 5, you can only name variables with Latin letters. Chinese characters are not supported, but you can name variables with English letters or pinyin.

![codey](../.gitbook/assets/30%20%281%29.png) ![codey](../.gitbook/assets/31%20%281%29.png)

* Use the following block to draw up a rabbit.

![](../.gitbook/assets/32.png)

![](../.gitbook/assets/33.png)

* Set the variable to the x coordinate of the image.

![](../.gitbook/assets/34.png)

* Add another script where the variable can be changed when a button is pressed. You can observe how the image changes and you can find that the rabbit will move out of the screen if the variable exceeds a certain value.

![](../.gitbook/assets/35.png)

* Now, finish the script. Rotate the images and change the coordinates. Look! The rabbit is running!

![codey](../.gitbook/assets/36.png) ![codey](../.gitbook/assets/37.png)

![](../.gitbook/assets/38.png)

Tip: Duplicate the image block and then make some changes of it. In this way, you can make an animation with minimal fuss.

**6.Display Sensor Values** _**（Intermediate）**_

codey has sets of sensors and can thus detect environmental changes around, including volume, light, gesture, etc.You can get access to sensor values in the following two ways:

* Please ensure that your device is well connected first. Then select the value that you want to get and show it on the Stage.

![codey](../.gitbook/assets/39.png) ![codey](../.gitbook/assets/40.png)

* You can also use the script as below and show the sensor values on the screen of codey.

![codey](../.gitbook/assets/41.png) ![codey](../.gitbook/assets/42.png)

* Upload the above-mentioned program to the device. Next, make some sounds to codey. Look, the value on the Stage and screen is changing.

Tip: Add a Wait block in the Repeat block to slow down the value change on the screen.

![](../.gitbook/assets/43.png)

**7.Volume Indicator** _**（Intermediate ）**_

With the image coordinate and the sound sensor, you can ensure a dynamic display of the volume on the codey screen:

* Connect the device. Select the Volume block and check for the volume in the current environment\( values may be different in other environments\).

![codey](../.gitbook/assets/44.png) ![codey](../.gitbook/assets/45.png)

* Use the following block to draw up a simple image.

![](../.gitbook/assets/46.png)

![](../.gitbook/assets/47.png)

* Use the arithmetic blocks under the Operators block category to get the volume values.

![](../.gitbook/assets/48.png)

![](../.gitbook/assets/49.png)

* Finish the program and upload it. Now you can yell at your codey and check if it works.

![](../.gitbook/assets/50.png)

Tip: You can regulate the value with the Multiple block while observing the volume change at the same time.

![](../.gitbook/assets/51.png)

**8.Avoid Obstacles** _**（Advanced）**_

If you want to get started with functions of rocky, you need to add the rocky extension in the mblock 5 first.

![](../.gitbook/assets/52.png)

![](../.gitbook/assets/53.png)

In this project, codey rocky and its sensor will be needed.codey rocky has an IR color sensor that can be switched forward or downward. In this project, you need to switch the IR color sensor forward as a way to detect the obstacles in front of codey rocky.

![](../.gitbook/assets/54.png)

All the blocks for this sensor are tagged with a sensor icon.

![](../.gitbook/assets/55.png)

* The following block is needed in this project.

Explanation: If an obstacle can be detected in front of the IR color sensor, the result for this block will be “true”, otherwise it will be “false”.

![](../.gitbook/assets/56.png)

Receive IR Send IR

Note: The fundamental principle for obstacles detection lies in the IR reflection. When obstacles detection is under way: the lighter the color of object is , the longer the distance is; the darker the color of object is, the shorter the distance is.

* Finish the following program. You can place obstacles in front of codey rocky to observe how its face will change.

![](../.gitbook/assets/57.png)

* Complete the program. Ensure that codey rocky will move on when no obstacle is detected, and turn right when obstacles are detected.

![](../.gitbook/assets/58.png)

**9.Interact with Stage Sprites: Control Musical Instruments with Broadcast**_**（Intermediate）**_

The Broadcast function can empower codey to communicate with sprites on the Stage. In this way, you can accomplish your interactive stage projects:

![](../.gitbook/assets/59.png)

* Create a New Message: When button A is pressed, broadcast A.

![](../.gitbook/assets/60.png)

![codey](../.gitbook/assets/61.png) ![codey](../.gitbook/assets/62.png)

* Add a sprite. The new sprite will show up in the Stage Area.

![](../.gitbook/assets/63.png)

![](../.gitbook/assets/64.png)

![](../.gitbook/assets/65.png)

* Click on the new sprite\(drum\) and make a program for it.

![](../.gitbook/assets/66.png)

![](../.gitbook/assets/67.png)

* Click on codey and upload its program to the device. Then, if you press the button A, you can hear drumbeats from the sprite drum on the computer.

![codey](../.gitbook/assets/68.png) ![codey](../.gitbook/assets/69.png)

* Similarly, you can add more musical instruments sprites. Let’s have a concert for Panda!

![](../.gitbook/assets/70.png)

**10.Communicate Variable and Gear Potentiometer** _**（Advanced）**_

The Broadcast function is just one option. You can make codey interact with the stage by creating a communicate variable as well.

In this project, you can use the gear potentiometer of codey to change the sprite size:

* Create a Communicate Variable

![](../.gitbook/assets/71.png)

![](../.gitbook/assets/72.png)

* Set the Communicate Variable to the value of gear potentiometer.

![](../.gitbook/assets/73.png)

* Click on the sprite Panda and you will find the communicate variable shows up in the data area as well.

![](../.gitbook/assets/74.png)

* Set the sprite size to the communicate variable value.

![](../.gitbook/assets/75.png)

* Upload the program of codey to the device and click the green flag. Pluck the gear potentiometer and observe how the srite changes.

![](../.gitbook/assets/76.png)

