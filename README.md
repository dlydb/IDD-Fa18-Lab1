# IDD-Fa18-Lab1: Blink!

**A lab report by Ziyu Liu**

## Part A. Set Up a Breadboard

[a photo of breadboard setup](//github.com/dlydb/IDD-Fa18-Lab1/blob/master/part_a.jpg)


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**
Brown Black Brown
 
**b. What do you have to do to light your LED?**
Press the push buttom.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
digitalWrite(LED_BUILTIN, HIGH); (make the LED on)

**b. What line(s) of code do you need to change to change the rate of blinking?**
delay(1000); (for both on and off time)

**c. What circuit element would you want to add to protect the board and external LED?**
 resistor
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
15 ms

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**
[blink code](//github.com/dlydb/IDD-Fa18-Lab1/blob/master/part_c_e.ino)


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[video](//youtu.be/HSp0EdomSaQ)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
Yes. Because there is a 220 ohm protect resistor connected to LED.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
Change the led pin to pin 11.

**b. What is analogWrite()? How is that different than digitalWrite()?**
Write the analog signal to the pin (from 0 to 255).
For digital, you can only use 0 and 1 for high and low (1 bit). 
For analog, you can use range from 0 to 255 to represent from low to high (8 bit).

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 
[schematic](//github.com/dlydb/IDD-Fa18-Lab1/blob/master/part_f.jpg)

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**
Yes. There is a microcontroller power with a USB input and read from a touch pad and send output signal to the LED with color and brightness of the light. The "computer" take input signal and control the output with input signal.

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**
Yes. The sensors are used to check if the buttom has been touched or not. The sensor will convey the signal to the microcontroller to tell it if the buttom is touched or not, for example, it may tell the microcontroller low when not touched, but when someone touched the touch pad, it will tell the controller that the voltage is high.  

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**
The device uses a USB as power supple. Yes. The chip transfers input from USB to power and ground. The system uses 3.3V as input voltage.

**d. Is information stored in your device? Where? How?**
Yes, there is. The information is stored in the capacitors to store the previous setting, such as color and brightness of last use. 

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.
The device is a desk lamp, so the most convinent way is to connect the LED to the output of the wire that the LED is in parallel with the LED from the lamp. 

### 3. Build your light!
[video](//www.youtube.com/watch?v=9yAfd1E-7Lg)
