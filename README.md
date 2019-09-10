# IDD-Fa19-Lab1: Blink!

**Zachary Gittelman Lab1 Report**

## Part A. Set Up a Breadboard

![Breadboard](https://github.com/zachgitt/IDD-Fa18-Lab1/blob/master/breadboard.jpeg)

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?** <br>
100 Ohm = Value x Multiplier + Tolerance = 1x100 + Tolerance <br>
Value = 1 = Brown <br>
Multiplier = 100 = Red <br>
Tolerance = N/A = Any Color <br>
 
**b. What do you have to do to light your LED?** <br>
The LED was lit up when the arduino was powered, and the circuit was complete starting from 5v on the arduino, through the button (pressed), through the LED, through the resistor, to ground on the arduino. The light did not originally work as the LED short leg and long leg were reversed. Placing the longer LED leg to positive and shorter leg to negative allowed for the LED to light properly.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?** <br>
The arduino > basic > blink example did not need to be modified as it already had the LED blink on and off. 
```c
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

**b. What line(s) of code do you need to change to change the rate of blinking?** <br>
By changing the delay times, we can modify how long the LED stays on and off.

**c. What circuit element would you want to add to protect the board and external LED?** <br>
By adding a resistor, we would protect the board from short circuiting.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?** <br>
The blinking seems indistinguishable at roughly 10ms. However by record the LED in slow motion I verified that it was still blinking.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.** <br>
[Blink Code](https://github.com/zachgitt/IDD-Fa19-Lab1/blob/master/blink.ino)


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**
Hitting raw from the video link will download the file.
[Blinking Video](https://github.com/zachgitt/IDD-Fa19-Lab1/blob/master/blinking_vid.mov)


## Part D. Manually fade an LED
**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?** <br>
The LED will go from dimly glowing to full brightness when turning the potentiometer because as we turn the knob the resistance decreases.

## Part E. Fade an LED using Arduino
**a. What do you have to modify to make the code control the circuit you've built on your breadboard?** <br>
Send the digital signal through a pin that is compatible. In this case I sent the signal through pin 13 by setting pinMode() to pin 13 and the two digitalWrite()'s to pin 13.

**b. What is analogWrite()? How is that different than digitalWrite()?**
While digitalWrite() can only send a HIGH or LOW Signal, analogWrite() can send a pulse width modulation signal which turns on for a specified duration in a given cycle length. 

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 
**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"** <br>
I took apart a mouse which has a sensor to read shifts in the light to determine the direction the mouse is moving. This sensor is connected to a computer on the mouse which calculates direction. 

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?** <br>
There is a light sensor. The output of the sensor is shared with the computer on the mouse.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?** <br>
The device is powered through USB. The power source is therefore the battery from attached computer. The power drawn through USB is 5V which does not appear to be transformed in the mouse. However resistors on the board regulate the power as the mouse moves the red light gets brighter.

**d. Is information stored in your device? Where? How?** <br>
Yes, the on board computer has memory to store previous images to determine the direction of movement.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.
I soldered a positive lead, LED, resistor, and negative lead to a resistor on the mouse. By originally connecting the negative lead to ground on the arduino I could determine a good position for the positive lead on the board. And by connecting the positive lead to 5V on the arduino I could determine a good position for the negative lead on the board. I determined this because the LED would like up if the lead was connected properly.

### 3. Build your light!

**Make a video showing off your Frankenlight.**
[Mouse Frankenlight]()

**Include any schematics or photos in your lab write-up.**
[Schematic]()
