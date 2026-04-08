# Little journal because I forgot to use Lapse...
## Falstad ideas and simulation 07/04 and 08/04 --> 1h30

First thing I made:
Using Falstad to try understanding active components such as transistors, helped by the week 2 guide.
I started by creating simple circuits to get familiar with NPN and PNP transistors. I built a basic transistor switch circuit first, connecting the base through a 10kΩ resistor to control an LED load on the collector. I experimented with different base resistor values (1kΩ, 4.7kΩ, 10kΩ, 22kΩ) to see how they affected the switching behavior and observed the voltage drops across each junction using Falstad's real-time voltage display. I also tried a Darlington pair configuration to understand current amplification better.
Then I moved on to the astable multivibrator model that was in the guide. I first made a first try and spent 30 minutes trying to make something but it was unsuccessful... I struggled with choosing the right capacitor values (started with 1µF which made oscillation way too slow), had issues with the transistors not switching properly because my base resistors were too high (I initially used 100kΩ), and couldn't get a stable oscillation pattern. The LEDs would either stay constantly on or flicker erratically.
Then, I made a second try the day after and this time it took me 1 hour before having something great: the logical following step: making an improved version of the astable multivibrator!
I started fresh with the classic configuration: two 2N2222 NPN transistors, 10kΩ base resistors, 100kΩ timing resistors, and 10µF electrolytic capacitors for the RC timing network. Once I got the basic circuit oscillating properly (which I calculated and verified with the scope view), I began experimenting with improvements.


The first try on falstad (tried other things but it was a fail) https://lapse.hackclub.com/timelapse/qOix7g-3-TwW
The second try on falstad: https://is.gd/G7ro6Q (tried other things but had the good result after) https://lapse.hackclub.com/timelapse/xlNTRmFHFsBe


## KiCad Schematic making 08/04 --> 0h30
After finishing my simulation, I went on KiCad and created a new project to start making the schematic.
It was pretty simple thanks to the wiring diagram made previously on Falstad. I started by placing the power symbols (VCC and GND), then added both BC547B transistors (Q1 and Q2) from the KiCad library. I carefully placed each resistor (R1-R4 for the base resistors and timing resistors, R5-R6 as current limiters for the LEDs), making sure to label them clearly with their values and designators.
For the capacitors, I added C1 and C2 and made sure to specify the polarity correctly in the symbol properties. The LEDs were placed with proper polarity indicators.
I spent extra time organizing the schematic "hierarchically" (crazy word lol) as in the falstad schem. Finally, I ran the Electrical Rules Check (ERC) which showed 0 errors and 2 warnings about power pins not being driven, which I resolved by properly connecting the symbols.


## KiCad PCB making 08/04 --> 1h
After finishing the schem and associating each symbol to an actual footprint, I could finally go to the most interesting part: The PCB design!
The footprint association took about 10 minutes.

I have chosen the way each components would be (changed a lot of times due to my incapacity of making choices...) and started the wiring process.
My first layout attempt had all components in a straight line, which looked boring and made routing difficult. Second attempt: I tried a circular arrangement with the LEDs at opposite ends, but the traces were crossing everywhere and would've needed too many vias. Third try: I arranged components in a shape with the battery holder at the bottom center, transistors in the middle, and LEDs in lines in the sides, but the trace lengths were unbalanced.
I made 4 tries to wire everything before having what seemed correct to me:

Try 1: Auto-router attempted but created messy traces with 90° angles
Try 2: Manual routing, top layer only, but had 3 airwires I couldn't resolve without crossing
Try 3: Two-layer design with ground plane on bottom, signal traces on top, but the ground plane had too many cutouts and wasn't continuous
Try 4: Final version with smart component placement.


<img width="420.5" height="379.5" alt="Capture d'écran 2026-04-08 173227" src="https://github.com/user-attachments/assets/756aae17-9132-461e-935d-c7d370067dab" />


I ran the DRC (Design Rule Check) and fixed all clearance violations by moving a few traces and adjusting the ground plane keepout zones.
WOW the whole thing was almost finished!


## Although, it was missing the MOST IMPORTANT PART: the silkscreen!! 08/04 --> 1h

It was a fun moment choosing the design and I ended up doing something pretty simple with the Hack Club logo (we represent of course), police-badge images, outlines, my website url everywhere (little publicity in passing), and the name of the board (I found a pretty font!!)
I started by importing the Hack Club logo and police badge images as an SVG, converted it to silckscreen using the KiCad tool, and placed it prominently in the top-center of the board at. Below that, I added "TTL SIREN" in the "AMIRI" font which gives that technical/electronic aesthetic I wanted. I created a double outline around the entire board perimeter to give that official badge framing effect.
I placed my website URL "gabintavernier.com" at the bottom in 1.5mm text, repeated it on the back side as well for maximum visibility. I also added component reference designators for each part (R1-R6, C1-C3, Q1-Q2, D1-D2) in 0.8mm text next to each footprint for easy assembly reference.
For the battery holder, I added a large "+" and "-" symbol (2mm height) to clearly indicate polarity, because I didn't want to destroy a transistor by accident during assembly!
On the back silkscreen, I added again police badge images and petter griffin as a cop.

I spent probably 20 minutes just tweaking the text sizes, positions, and trying different fonts before settling on the final layout. The silkscreen added so much personality to what would've been just a boring green PCB!


<img width="300" height="331" alt="Capture d'écran 2026-04-08 190014" src="https://github.com/user-attachments/assets/409f6b55-a5b5-4880-baf3-d5acffd4d5ab" />
<img width="316" height="321" alt="Capture d'écran 2026-04-08 185930" src="https://github.com/user-attachments/assets/1fafd53f-dddd-44aa-929d-c742237f4b45" />


The board is finished!! I then uploaded every files to my repo: generated Gerber files (F.Cu, B.Cu, F.Silkscreen, B.Silkscreen, F.Mask, B.Mask, Edge.Cuts), drill file (.drl), BOM (Bill of Materials in .csv format with all component values, designators for ordering), and the full KiCad project files (.kicad_pro, .kicad_sch, .kicad_pcb).
I created a detailed README.md, and made all the things I had to do in it. SO BORING!! (just kidding I love this part too lol)
Finally, I submitted everything to the Resolution project tracker. Total time logged: 4 hours of pure electronics design joy!


### Thanks RESOLUTION for this project!!
see yall
