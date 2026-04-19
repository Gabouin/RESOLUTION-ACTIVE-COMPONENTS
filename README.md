# TTL BASED POLICE SIREN
<br>

## [FALSTAD](https://is.gd/G7ro6Q) SIMULATION 


![astable gif](https://github.com/user-attachments/assets/3a7efbe8-ae42-4320-8a09-c7cf85e7c0d8)

#### The two transistors alternately switch on and off because when one transistor turns on, it prevents the other from conducting by pulling its base voltage low. The capacitors charge and discharge through the resistors, creating a timing delay that makes the transistors switch states repeatedly, causing the LEDs to blink back and forth, like a siren.
#### My final TTL circuit is basicaly an astable multivibrator that is meant to look like a **police siren** !
#### I choose to make that because I was stuck looking for an idea and ended up having this popping in my head and I tought it would be fun to add in a 3D printed translucent enclosure to make maybe a real-looking police siren for cosplay.
<br>  

## SCHEM DESIGN

I made the schematic on KiCad :

<img width=100% alt="image" src="https://github.com/user-attachments/assets/2f5d31db-122c-426a-85ea-819e03e0c495" />

## PCB DESIGN 

### Components placement

I made an edge cut's shape based on a police siren and put all the components inside to have the blue LEDS on one side and the red LEDS on the other side, the other components in the middle with still somewhere to add silkscreen.  

<div align=center>
  <img width=50% alt="image" src="https://github.com/user-attachments/assets/bf18229f-c8a7-4f27-bb7d-6c9a849f000b" />
</div>

### Silkscreen

<div align="center">
  <table>
    <tr>
      <td valign="bottom"><img width=100% alt="Capture d&#39;écran 2026-04-08 185900" src="https://github.com/user-attachments/assets/869ec768-26f9-442d-971c-4dbc7006351f" /></td>
      <td valign="bottom"><img width=100% alt="Capture d&#39;écran 2026-04-08 185930" src="https://github.com/user-attachments/assets/c051fb0c-fd69-4023-a1f7-cc7fef2344a6" />
</td>
      <td valign="bottom"><img width=100% alt="Capture d&#39;écran 2026-04-08 190022" src="https://github.com/user-attachments/assets/572d5b29-a6d5-45bb-a892-da4b09a51ae9" /></td>
      <td valign="bottom"><img width=100% alt="Capture d&#39;écran 2026-04-08 190014" src="https://github.com/user-attachments/assets/f27498d0-91bf-4ecd-8b05-4e4a250a9040" /> </td>

  </table>
</div>





_____________________________________________________________________________________________________________________________________________


#### This project was made for the 2nd week of RESOLUTION - Hack Club

Please take in conscious that lapse (and so hackatime) was only used for the falstad simulation (1 hou) but for the other steps I forgot to use it so the time wasn't counted and the Schem and PCB took me aprox 3hours
