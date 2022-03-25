# Ala-Carte

## Table of Contents 

# Classes, Objects, And Modules 
# (Fade LED Code)

```python

import time
import board
from rgb import LED   # import the RGB class from the rgb module

r1 = board.D7
g1 = board.D4
b1 = board.D3

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
    
    ```
