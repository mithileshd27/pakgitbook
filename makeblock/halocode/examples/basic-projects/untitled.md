# Untitled

**Compare Strength**

**Programming Result**

![](../../../../.gitbook/assets/0.gif)

**Introduction to HaloCode's motion sensor**

The motion sensor detects how HaloCode moves, including shaking strength.

![](../../../../.gitbook/assets/1%20%2847%29.png)

**Set the range of shaking strength**

1. Drag an Operators block \(\) &gt; \(\) to the Scripts area, and change the value of the second parameter to "30". Add a Sensing block shaking strength to the first parameter.

![](../../../../.gitbook/assets/2%20%282%29.gif)

2. Add a Control block if \(\) then \(\).

![](../../../../.gitbook/assets/3%20%283%29.gif)

**Set LED animation**

3. Add a Lighting block all LEDs light up \(\), and a Control block wait \(\) seconds. Add another Lighting block light off all LEDs to light off all LEDs in 1 second.

![](../../../../.gitbook/assets/4%20%283%29.gif)

4. Likewise, for shaking strength greater than 60, we can duplicate the script. Change the value to 60 and LED color to red.

![](../../../../.gitbook/assets/5%20%281%29.gif)

**Add event and control**

5. Add an Events block when HaloCode is shaking and a Control block forever.

![](../../../../.gitbook/assets/6.gif)

**Read shaking strength**

6. Check the box for Sensing block shaking strength.

![](../../../../.gitbook/assets/7%20%281%29.gif)

7. Shake HaloCode! See if you can make the LED ring light up red.

