# Rainbow Star Christmas Tree Topper

[I made a glowing rainbow Christmas tree topper](https://www.youtube.com/watch?v=D-ZuGpuFYso), and I've been asked to share the design.

This has not been designed as a consumer-ready product but as something just for me, so it requires some glue and fiddling to assemble, and it's a little fragile.

I'm providing no guarantee/support for this at all :)

## Print

If you'd like to print it as-is, the STL files are what you need. I have provided these as separate files for each of the four parts.

If you want to tweak it, I've provided the .f3d design file. I modelled it in Fusion360 with the main measurements done parametrically (but some of the bits have been done statically). It'll probably be fine if you scale up but i think it'll break if you scale down. Good luck.

## Assemble

### Materials

* My four 3D printed star parts
* Glue
	* Super Glue (also known as Cyanoacrylate)
	* Bostik All Purpose glue. (it's like a contact adhesive for home/craft use, that holds well but comes apart again relatively easily.)
* Some LED strip
	* I used: 12mm 60ppi Dotstar/APA LED strip.	* You can use basically anything for this but I used what I had to hand.
	* My scavanged strips were a bit short at ~35 LEDs, but it still looks fine.
	* Neopixel/WS2812 strip will be more straightforward as it has one fewer wire, and many microcontrollers have a default output for this.
* A Microcontroller
	* I used: Adafruit Qt Py SAMD21.
	* You can use basically anything for this but I used what I had to hand.
* A way to connect the LED strip to the Microcontroller.
	* I used: A StemmaQT/Qwiic cable, chopped in half and soldered onto the end of the LED strip.
		* Whether this is Proper or not I don't know, but my type of strip needed Power, Ground, Data and Clock signals, and the microcontroller I used had pins capable of all 4 on a handy connector, which makes it a bit easier to use for me than soldering the two together, and there's no real standard small LED-to-microcontroller connector that I know of.
		* The way I'd've done this "normally" on a board without this connector would be to solder wires directly from the LEDs to the microcontroller board.

### Steps

1. Print the 4 pieces on a 3D printer.
	* I used white PLA filament, 0.4mm nozzle, 0.16mm layers, and tree supports.
1. Put together your LEDs and Microcontroller and check they work.
1. Put the Star Lid and Base Top to one side.
1. Attach the LEDs around the edge of the Star Body part, pointing inwards.
	* I used Bostik All Purpose glue for this because it works and is removeable.
1. Attach the Base Bottom to the Star Body.
	1. Use Super Glue around the recessed top edge of Base Bottom .
	1. Place inside the bottom hole of the Star Body, lining up the edges as best you can.
	1. Hold it for 30s+ to set. Don't rest it on a table until it's set because it'll lever the base part off the star.
1. Attach your LED cabling in and test.
	* I put my microcontroller inside the base, and taped it in place to provide some strain relief.
	* Attach your power cable now.
1. Glue the Star Lid onto the Star Body.
	1. Identify the five mounting pegs at the end of every star point.
	1. Add a small blob of Bostik All Purpose to the top of each peg.
	1. Put the Star lid on and apply some light pressure for 15+ seconds for it to stick.
1. Test the electronics all work and look pretty.
1. Attach the Base Top.
	1. Identify the four mounting pegs on the Base Bottom.
	1. Add a small blob of Bostik All Purpose to the top/outsideside of each peg.
	1. Apply Bostik All Purpose around the recessed top edge of Base Top.
	1. Slide the top edge of Base Top into the Star's hole.
	1. Lower the piece until it rests neatly on top of the mounting pegs.
	1. Carefully hold it in place for 15+ seconds so the two base pieces align well.
1. Test the electronics.
1. Put it on your tree. wooo!


## Code
I'll upload it at some point but it depends heavily on what LEDs and microcontroller you use.

My code is just copy-pasted from an Adafruit tutorial for CircuitPython and Dotstar LED strips.