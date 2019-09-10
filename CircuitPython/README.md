# CircuitPython

All of my CircuitPython code is here.

## Overview of all code

The CircuitPython code in this repository is run on a fancy little thing called...
> ...a Metro M0 Express and at first glance, you might think it's just an Arduino with a new paint job.  Au contraire!
>
> ![Picture of the Metro M0 Express.](https://cdn-shop.adafruit.com/970x728/3505-06.jpg "The Metro M0 Express")
> 
> [Source](https://cvilleschools.instructure.com/courses/26602/assignments/173747?module_item_id=480883)

The Metro M0 Express is specifically designed for CircuitPython - a version of Python. You could say it's pretty neat, if you felt so inclined.

Here's a brief rundown of each file:

### [fade.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/fade.py)

[fade.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/fade.py) is a very basic file with the purpose of making an LED fade On and Off.
That's pretty much it. The code is not too complicated - only difficult bit was understanding how the PWMOut object operated - after that it's basic Python loops if statements

### [lcd_assignment.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/lcd_assignment.py)

[lcd_assignment.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/lcd_assignment.py) is a file with the purpose of displaying a number that would increase by different modifiers when a button was pushed based on the current modifier (also determined by a button). I also included
a reset button that reset the modifier to 1 and number to 0 because that's just how quirky I am. The only part of this assignment that was a pain was the lcd libraries and the apparent lack of memory for
the poor Metro M0 Express. Updating the libraries and clearing it of uneccesary junk was tedious but was effective in the long run.

### [photo_interrupter.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/photo_interrupter.py)

[photo_interrupter.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/photo_interrupter.py) is a file that spits out the number of interrupts
a photo_interrupter has experienced every four seconds (without using the time.sleep() function).
The main difficult part of the assignment was checking only every four seconds without using the aforementioned function, making me use some very messy and unconventional methods of variable comparison that I'm afraid
has just become my style of code.

### [pot_rgb_adjusters.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/pot_rgb_adjusters.py)

A fun just-for-kicks assignment where you can change the neopixel color with three potentiometers for r, g, and b values.

 


