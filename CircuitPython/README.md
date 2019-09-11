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
That's pretty much it. The code is not too complicated; the only difficult bit was understanding how the PWMOut object operated. After that it's basic Python loops if statements

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

### [sensor.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/sensor.py)

[sensor.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/sensor.py) was a super fun assignment (there's no sarcastic font but just use your imagination).
The assignment was to have a sensor read the distance between itself and the closest object, changing the
neopixel color along a spectrum as the sensor distance gets higher. The sensor wasn't too complicated to code, and looking 
at the HCSR04 library told me how to use it. The red, green, and blue color spectrum had me scratching my head for a little while, but in the end
I found a clean(ish) solution.

    if dist <=15:
        r = 255-(17*dist)
        b = 0+(17*dist)
        g = 0
    
    elif dist > 15:
        b = 255-(17*(dist-15))
        g = 0+(17*(dist-15))
        r = 0

Essentially "mapping" the values gotten from the sensor to possible r, g, and b values neatly accomplished the objective.

### [servo_touch.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/servo_touch.py)

[servo_touch.py](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/servo_touch.py) is the code for an assignment where touching
one wire moves the servo in one direction while touching the other wire moves the servo in the opposing direction. I spiced up the assignment
a small amount by changing the neopixel color depending on what color the servo was turning. The only strange part about the assignment
was learning about how TouchIn objects functioned, but it was smooth sailing after that.

##Other Files

There are just a few other files in the CircuitPython folder. Here is the brief overview of what each one does:

###[README.md](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/README.md)

The [README.md](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/README.md) is what you're reading right now. It
gives an overview of all the files in this folder and what their purpose is.

###[agenda.md](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/agenda.md)

The [agenda.md](https://github.com/clyman88/Engineering-3/blob/master/CircuitPython/agenda.md) is currently a list of what needs to be done
in the CircuitPython folder. Formatting is in progress to be more easy to use and make it more perdy.


![That's all folks!](https://cdn10.bigcommerce.com/s-btntxk/products/115/images/506/0002002301.2_IMG_1792_3__56379.1444757924.1280.1280.JPG?c=2 "That's all folks!")

