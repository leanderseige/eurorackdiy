# A Power Supply for my DIY Eurorack

**WARNING! This device operates with high voltage. This is life-threateningly dangerous! This is a documentation. Not a manual. I may have made mistakes. If you try to build a similar device, the entire risk is yours alone! If you don't have training or don't feel 1000% confident in handling high voltage, DON'T DO IT and buy a safe, industrially manufactured device.**

If you find mistakes or suggestions for improvement, please don't hesitate and send them my way.

## The Power Supply

Here is the documentation of how I  built my own Eurorack DIY power supply, including an appropriate case.

<img src="photos/psu.jpg" width="600">

<img src="photos/psuinside1.jpg" width="300" style="display:inline-block;"> <img src="photos/psuoutside1.jpg" width="300">

## Circuit Diagram

I chose this circuit as a basis for my power supply: https://syntherjack.net/modular-synth-power-supply/

However, I have made a few small changes. So here is the diagram of exactly my PSU:

<img src="bitmaps/psu_circuit_diagram.png">

Various Comments:

In order to get a full featured PSU I simply added a 7805 to the 12V channel to create a 5V channel. But I didn't want the 7805 to be all alone so I placed some additional capacitors around it.

I had a rectifier RS405 at hand from an old PC power supply, so I chose this one.

I did not have 1N4007 diodes but UF4007, so I used these instead.

I have one of those complete power modules that consist of a switch, a fuse and a jack and I used it for the rear side of the PSU (https://amzn.to/3XVcw57). Of course I also added another switch for the front panel so I ended up with two switches.

I did not feel save with just one fuse in the primary circuit so I added one in each secondary AC channel. This maybe could or should be improved by putting them on the DC outputs instead?

I was not able the get the output voltages lower than 12.7 (or -12.7) volt. So next time I probably would try a 1.5k resistor plus a 1k potentiometer. However I did not measure the PSU with load yet.

There are three control LEDs on the front panel of the power supply. I chose the colors according to the ATX standard (https://en.wikipedia.org/wiki/ATX) : yellow for +12V, red for +5V and blue for -12V.

<img src="photos/psuoutside2.jpg" width="300">

## Transformer

In order to make sure that both secondary windings are connected in the same order
I checked using my oscilloscope. I did not confirm it experimentally but I am sure
that the secondary windings must be connected in the right phase order. The following
screenshots show the two options of the phases and I chose the right option because
I am sure that this is the only correct way to do it.

![](bitmaps/oscilloscope1.png)

I used this toroidal mains transformer: https://www.reichelt.de/ringkerntrafo-80-va-2x-15-v-2x-2-67-a-rkt-8015-p15283.html

## Case

I decided to design a complete case for my PSU and manufacture it with my 3d-printer (https://amzn.to/3wCqKfW) using black PLA (https://amzn.to/3Dog1cx). Here is the model of it:

![](bitmaps/explodedpsucase.png)

The case was made to be placed into a Eurorack and requries 36HP. It is divided into two chambers: the first one contains all the high voltage elements and the transformator while the second one houses the voltage regulator board. Outside the case is a niche for a small PCB with up to three 16pin sockets.

<img src="photos/psuinside2.jpg" width="300"  style="display:inline-block;">

There is also a rectangluar window for a grille of 10cm x 10cm to let warm air escape. I bought one of these perforated Aluminium sheets to use it as grille: https://amzn.to/3iXulSA The windows were placed inside the chassis area to avoid screws protruding into the adjacent module space.

<img src="photos/psubuiltin.JPG" width="300">

The high voltage chamber has a round bed for a toroidal transformer.

The upper element is provided with recesses into which nuts can be glued. But I also had to remove some plastic here and there in order to give the skrews enough space.

<img src="photos/psutop.jpg" width="300">

There is also a small element to fix a power cable inside the Eurorack case (Zugentlastung).

<img src="photos/cable.jpg" width="300">

There is a separate 3D model of a support element to be placed below the PSU so the weight of it does not bend any of the other elements over time. I made this supporting element not exactly as high as required because I planned to glue some rubber (https://amzn.to/3wzfgJU) onto it.

<img src="photos/support.jpg" width="300">

## What would I change if I would build this a second time?

- Make the right side rear wall one millimeter thicker so it does bend less wenn pluging/unpluging the power cord.
- I didn't need the hole for the front panel fuse, so I would close it. However, it could be useful with a different design.
