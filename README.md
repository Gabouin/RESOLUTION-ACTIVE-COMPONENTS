# TTL BASED POLICE SIREN
__________________________________________________
## SIMULATION

First schem on falstad, using the guide : https://is.gd/lMH7cU 
<img width="1051" height="667" alt="image" src="https://github.com/user-attachments/assets/434c343c-6b33-4609-97b4-3fcaf0b3e08a" />

____________________________________________________________________________________________________________________________________________________________________


After that, the logical following step was to make an improved version of the atsable multivibrator ! 

The first try on falstad (tried other things but it was a fail) https://lapse.hackclub.com/timelapse/qOix7g-3-TwW

The second try on falstad : https://is.gd/G7ro6Q (tried other things but had the good result after) https://lapse.hackclub.com/timelapse/xlNTRmFHFsBe

![astable gif](https://github.com/user-attachments/assets/3a7efbe8-ae42-4320-8a09-c7cf85e7c0d8)

### The two transistors alternately switch on and off because when one transistor turns on, it prevents the other from conducting by pulling its base voltage low. The capacitors charge and discharge through the resistors, creating a timing delay that makes the transistors switch states repeatedly, causing the LEDs to blink back and forth, like a siren.
### My final TTL circuit is basicaly an astable multivibrator that is meant to look like a **police siren** !
### I choose to make that because I was stuck looking for an idea and ended up having this popping in my head and I tought it would be fun to add in a 3D printed translucent enclosure to make maybe a real police flashing light for cosplay.

## SCHEM DESIGN

I made the schematic on KiCad :

<img width="907" height="632" alt="image" src="https://github.com/user-attachments/assets/2f5d31db-122c-426a-85ea-819e03e0c495" />

## PCB DESIGN 

I made an edge cuts' shape based on a police siren and put all the components inside to have the blue LEDS on one side and the red LEDS on the other side, the other components in the middle with still somwhere to add silkscreen. I made 4 try to wire everything before having what seems correct to me : 

<img width="841" height="759" alt="image" src="https://github.com/user-attachments/assets/bf18229f-c8a7-4f27-bb7d-6c9a849f000b" />

After that, I took fun making the silscreen ! 

Front one : 

<img width="711" height="733" alt="Capture d&#39;écran 2026-04-08 185900" src="https://github.com/user-attachments/assets/869ec768-26f9-442d-971c-4dbc7006351f" />
<img width="632" height="642" alt="Capture d&#39;écran 2026-04-08 185930" src="https://github.com/user-attachments/assets/c051fb0c-fd69-4023-a1f7-cc7fef2344a6" />


Back one :

<img width="638" height="716" alt="Capture d&#39;écran 2026-04-08 190022" src="https://github.com/user-attachments/assets/572d5b29-a6d5-45bb-a892-da4b09a51ae9" />
<img width="617" height="662" alt="Capture d&#39;écran 2026-04-08 190014" src="https://github.com/user-attachments/assets/f27498d0-91bf-4ecd-8b05-4e4a250a9040" />


_____________________________________________________________________________________________________________________________________________


### This project was made for the 2nd week of RESOLUTION - Hack Club

### Thank you to the whole team of reviewers !

