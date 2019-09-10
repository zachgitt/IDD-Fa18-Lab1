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

[Blinking Slomotion Video](https://github.com/zachgitt/IDD-Fa19-Lab1/blob/master/blinking_vid.mov)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

**b. What is analogWrite()? How is that different than digitalWrite()?**


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
