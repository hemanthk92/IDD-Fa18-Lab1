# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

[link to picture](basic_breadboard.JPG)


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

 If we use the 5 band resistor. 
 First Band - Brown, Second Band - Black, Third Band - Black, Fourth Band - Black, Fifth Band - Brown
 
**b. What do you have to do to light your LED?**

From the 5V pin we connect a cable to the positive line. From the positive line we connect a resistor to the cathode of the LED. The Led is then placed next to the switch. From the other end of the switch we pick up the charge pass to the negative line through a wire. Then we connect the negative line to the ground. 
Then we supply power to the circuit by connecting the board to the laptop. Then we click the switch to close the circuit which will cause current to flow and power the LED.

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
[link to video](https://www.youtube.com/watch?v=gv7c_gFRxzA&feature=share)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
Yes we are able to get the potentiometer to glow and fade with the LED. The potentiometer acts as a variable resistor. 

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
We use the analogwrite function as opposed to digital write function. In the analogwrite function we can specify a brightness.
And in order to make the light fade we loop through various brightness values.

**b. What is analogWrite()? How is that different than digitalWrite()?**
Analog write uses PWM so it sends current signal many times on and off in a second. digitalwrite produces a constant signal. 
<br >
[link to code](analog_fade.ino)

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 
[link to picture of schematic](schematic.jpeg)
<br >
I used a wireless keyboard from logitech. Here is a picture of the circuit with some labeled parts. The circuit is connected to a two double a batteries. The power then enters the PCB and flows through the power regulating devices. There is one large crystal osciallator and many resistors throughout the circuit. There are also wiring thats connect to the matrix of circuits behind individual keys. Key strokes on the board are then sent to microcontroller and then presumbly sent to connected laptop etc. 
<br >**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**
Yes there is a microcontroller that converts the location where the keystroke completes the circuit to a key on the keyboard. It then sends that key through the circuit and to the computer. 

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**
There are a grid of circuits underneath the keys of the keyboard. When a key is pressed the circuit below is completed and current flows through and back to the microcontroller. 

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**
There are slots for Double A batteries hook up that provide power. The batteries are connected to the circuit, since its 2 double A batteries the circuit through the system must be 3 volts. There is another point on the circuit labeled TP 3 2.2 V DC.
There is a capicitor and many resistors that regulate the power through the circuit. 

**d. Is information stored in your device? Where? How?**
Yes there is memory on the keyboard that maps each circuit in the matrix to a specfic letter on the keyboard. I could not find the memory on the PCB, the memory is probably built into the micro controller.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.
The keyboard has an on/off switch that we can use to hack. We can then use the switch to power on and off an external LED on our arduino board. I will take power from the arduino (laptop) and funnel it through the PCB on the keyboard and through the on/off switch. From the end of the circuit or the negative end I will connect the current back to the arduino board. 
**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**
[link to video](https://youtu.be/ObonbDq9Cnw)<br>
**Include any schematics or photos in your lab write-up.**
