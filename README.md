![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Project](https://img.shields.io/badge/Project-Hardware-yellow.svg)
![Series](https://img.shields.io/badge/Series-SPECIAL_ISSUE-red.svg)


<table>
  <tr>
    <td width="17%">
      <img width=100% alt="image" src="https://githubom/user-attachments/assets/d4c7bb2a-7c48-4c4c-b114-118e6000fbbe" />
    </td>
    <td>
      <h1>TTL Based Police Siren</h1>
      <p>
        A TTL logic circuit designed to mimic a police siren using an astable multivibrator. Blue and red LEDs alternate in a blinking pattern, with a custom          PCB shaped like a siren light. Designed to fit inside a 3D-printed translucent enclosure for a realistic cosplay prop.
      </p>
    </td>
  </tr>
</table>
---

## Table of Contents

- [About the Project](#about-the-project)
- [Circuit Simulation](#circuit-simulation)
- [Schematic Design](#schematic-design)
- [PCB Design](#pcb-design)
- [Bill of Materials](#bill-of-materials)
- [Production Files](#production-files)
- [License](#license)
- [Contributing](#contributing)

---

## About the Project

The core of this project is an **astable multivibrator** built from two NPN transistors. The transistors alternately switch on and off: when one turns on, it pulls the other's base voltage low, preventing it from conducting. The capacitors charge and discharge through the resistors, creating a timing delay that causes the transistors to switch states repeatedly — making the LEDs blink back and forth like a siren.

The PCB outline is shaped like a police siren light, with blue LEDs on one side and red LEDs on the other, and components grouped in the centre. The design is intended to fit inside a 3D-printed translucent enclosure for use as a cosplay prop.

> This project was made for the 2nd week of **RESOLUTION** — Hack Club.

---

## Circuit Simulation

An interactive simulation of the circuit is available on **Falstad Circuit Simulator**:

▶️ [Open the Falstad simulation](https://is.gd/G7ro6Q)

![Astable multivibrator simulation](https://github.com/user-attachments/assets/3a7efbe8-ae42-4320-8a09-c7cf85e7c0d8)

---

## Schematic Design

The schematic was designed in **KiCad**. Source files are available in the [`Sources/KiCad`](Sources/KiCad) folder.

<img width="100%" alt="Schematic" src="https://github.com/user-attachments/assets/2f5d31db-122c-426a-85ea-819e03e0c495" />

---

## PCB Design

### Component Placement

The PCB edge cut is shaped like a police siren. Blue LEDs are placed on one side and red LEDs on the other, with passive components grouped in the centre.

<div align="center">
  <img width="50%" alt="PCB component placement" src="https://github.com/user-attachments/assets/bf18229f-c8a7-4f27-bb7d-6c9a849f000b" />
</div>

### Silkscreen

<div align="center">
  <table>
    <tr>
      <td align="center"><img width="100%" alt="Silkscreen view 1" src="https://github.com/user-attachments/assets/869ec768-26f9-442d-971c-4dbc7006351f" /></td>
      <td align="center"><img width="100%" alt="Silkscreen view 2" src="https://github.com/user-attachments/assets/c051fb0c-fd69-4023-a1f7-cc7fef2344a6" /></td>
      <td align="center"><img width="100%" alt="Silkscreen view 3" src="https://github.com/user-attachments/assets/572d5b29-a6d5-45bb-a892-da4b09a51ae9" /></td>
      <td align="center"><img width="100%" alt="Silkscreen view 4" src="https://github.com/user-attachments/assets/f27498d0-91bf-4ecd-8b05-4e4a250a9040" /></td>
    </tr>
  </table>
</div>

---

## Bill of Materials

| Designator | Value | Footprint | Quantity |
|---|---|---|---|
| C1, C2 | 12 µF | C_Disc_D5.0mm_W2.5mm_P5.00mm | 2 |
| D1–D10 | LED | LED_D5.0mm | 10 |
| J1 | Conn_01x02 | PinHeader_1x02_P2.54mm_Vertical | 1 |
| Q1, Q2 | NPN | TO-92L_Inline_Wide | 2 |
| R1, R4 | 330 Ω | R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal | 2 |
| R2, R3 | 1 kΩ | R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal | 2 |

> The full BOM is also available as a CSV file in the [`production`](production) folder.

---

## Production Files

Gerber files, drill files, BOM, component positions, and netlist are available in the [`production`](production) folder, ready for PCB fabrication.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## Contributing

Contributions, improvements, and remixes are welcome! Please read the [CONTRIBUTING.md](CONTRIBUTING.md) guide to get started.
