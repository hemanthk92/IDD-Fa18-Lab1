# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

 If we use the 5 band resistor. 
 First Band - Brown, Second Band - Black, Third Band - Black, Fourth Band - Black, Fifth Band - Brown
 
**b. What do you have to do to light your LED?**

After setting up the circuit with a LED and switch we have to connect the arduino to a laptop as a power source. Then we click the switch to close the circuit which will cause current to flow and power the LED.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**<br />
The digitalwrite function turns the led on. this is at line 8 and 10.<br />
**b. What line(s) of code do you need to change to change the rate of blinking?**<br />
The delay function controls the stopping time in between the light flashing. This is on lines 9 and 11.<br />
**c. What circuit element would you want to add to protect the board and external LED?**
<br />
 You should add a resistor so you don't supply to much current to the LED and break it.
<br />
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
<br />
If the delay is <= 10, you cannot tell the light is blinking. 
<br />
**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.** <br />
[link to code](led_blink.ino)



### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
No we are not able to ge the LED to glow the range of the potentionmeter. Arudino cannot output an analog voltage.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
We use the analogwrite function as opposed to digital write function. In the analogwrite function we can specify a brightness.
And in order to make the light fade we loop through various brightness values.

**b. What is analogWrite()? How is that different than digitalWrite()?**
Analog write uses PWM so it sends current signal many times on and off in a second. digitalwrite produces a constant signal. 
[link to code](analog_fade.ino)

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
