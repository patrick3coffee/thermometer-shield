# The Idea
I wanted a display of temperature and humidity and it exploded into this shield that functions as a thermostat, humidistat, and optostat (if that's even a word).
This project is my first attempt at creating a pcb. The design work is done in KiCAD. 

## Logical units of functionality
1. Display: this 4 digit, 7-segment display is driven by shift registers and transistors.
2. ULN2804 breakout: a transistor array for controlling 8 resistive or inductive loads.
    * Channels A through D plus G and H terminate to screw terminals. Channels G and H are connected in parallel to A and B respectively. This increases current capacity
    * Channels E through H terminat to pin headers.
    * To use G and H independently, four traces must be cut on the bottom of the board and the exposed inputs must connect to a desired arduino pin.
3. Button Array: Four buttons alter the output voltage in an array of voltage dividers
4. Photoresistor: Measures light.
5. RHT03: Measure temperatre and humidity.
6. I2C pin headers: allow for greater hackability.
7. All unused pins exposed.
    * D9 and D12
    * A2 and A3.
    * A4 and A5 in I2C header, but can be used for any purpose.

## The progression of scope creep  
* Display temperature and humidity in garage. (done on a breadboard)  
* Do the same in the chicken coop.
* Make the hum/temp readings control things at specified thresholds.
* Make those thresholds settable on the front panel.
* Add a light sensor because the chicken coop needs the door shut at sunset and opened at sunrise.
* Expose all unused pins in useful ways for hackability.

