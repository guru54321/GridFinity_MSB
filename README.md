# GridFinity_MSB
A modular, searchable base for the searchable GridFinity project which Zack recently launched. This project is partly hardware, partly software based.
In this repository I try to document the design and build of a modular baseplate, used to integrate with the searchable index of the Gridfinity
See also Zack Freedman's video on this topic: https://www.youtube.com/watch?v=7WAhquGQq3o

Requirements:
Modularity: The design must be modular. Just like the original non-searchable base plates, it should be possible to link together multiple smaller baseplates to form a single, larger base plate.
Leds: Zack likes his leds so there will be leds. I intend to create a # of versions supporting simple leds (2 colours) or using a number of digitally controlled leds. 
price: I try to keep the costs of the project down as much as possible. I'll use standard components only.
Speed: It should be easy to build a large fleed of searchable bases. Assembly should be simple and fast.
Easy to solder: If possible (if it fits!) i'll try to design a  no SMD components version. I'll also try to dabble with SMD components though.

Main idea:
Zack uses a diode array to detect any tripped reed switch (just like a keyboard would). This is not very modular, as extending the grid always means more rows and columns (more wires!). I intend to use a shift bit register, Parallel In Serial Out (PISO) which allows me to use a single data-in line to read out all switches on a single module. It also allows me to string together multiple modules as a single larger module. By arranging the connections between the modules in a certain way, it should be possible to allow for extensions of a base plate in all directions.
The final layout of the grid (the total #of plates) should be configured in the micro processor, driving the whole thing. I intend to use an ESP32 as they are cheap and easy to aquire as wel program.

