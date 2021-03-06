# Ala-Carte

## Table of Contents 
* [Fade LED Code](https://github.com/aniyahmoore28/Ala-Carte#fade-led-code)

---

# Classes, Objects, And Modules 

# Fade LED Code

```python

import time
import board
from rgb import LED   # import the RGB class from the rgb module

r1 = board.D7
g1 = board.D4
b1 = board.D5

r2 = board.D8
g2 = board.D9
b2 = board.D10

myblueLED1 = LED(b1)
mygreenLED1 = LED(g1)
myredLED1 = LED(r1)

myblueLED2 = LED(b2)
mygreenLED2 = LED(g2)
myredLED2 = LED(r2)

# myRGB1 = RGB(r1,g1,b1)   # create a new RGB object, using pins 3, 4, and 5
# myRGB2 = RGB(r2,g2,b2)   # create a new RGB object, using pins 8, 9, and 10
while True:
    myblueLED1.fade()
    time.sleep(1)
    mygreenLED1.fade()
    time.sleep(1)
    myredLED1.fade()
    time.sleep(1)
    myblueLED2.fade()
    time.sleep(1)
    mygreenLED2.fade()
    time.sleep(1)
    myredLED2.fade()
    time.sleep(1)
   
```

---------
```python

#these are the libraries needed to fade an LED
import time
import board
import pwmio

class LED:

    #note: I had a blue led, so I named my incoming ardument "bluePin"
    def __init__(self, ledPin):
       # init = like void Setup() from arduino.  Initialize your pins here
       # start each object with "self.object"
       self.led = pwmio.PWMOut(ledPin, frequency=5000, duty_cycle=0)

    def fade(self):
        # write your code to make it fade, here
        for i in range(100):
        # PWM LED up and down
            if i < 50:
                self.led.duty_cycle = int(i * 2 * 65535 / 100)  # Up
            else:
                self.led.duty_cycle = 65535 - int((i - 50) * 2 * 65535 / 100)
            print(self.led.duty_cycle)
            time.sleep(0.01)
            
  ```


# Reflection
1) This project forced me to ask my classmates for help when i was struggling 
2) Helped me create problem solving skills
3) Made me realize i should be more careful when wiring my arduino because the smallest kink could stop it from working
4) I learned that class, and objects are important when you need to create your own class to import into the final code

# Evidence
<img src="https://github.com/aniyahmoore28/Ala-Carte/blob/main/images/fed%20LED%20Gif.gif" width="150" />

--------

# CircuitPython LCD


# Code

# Reflection


