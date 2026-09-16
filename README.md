# STM32-Mechanical-Keyboard
![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-blue.svg)
![Status](https://img.shields.io/badge/status-in--progress-yellow)
![Tech](https://img.shields.io/badge/MCU-STM32F103C8T6-blue.svg)


## Overview

This is a DIY mechanical keyboard built from scratch around the STM32F103C8T6 (Blue Pill), designed and implemented using the full STM32 development ecosystem (STM32CubeMX, STM32CubeIDE, STM32CubeProgrammer).

The goals of this project are to:
- Learn how to design and build a complete mechanical keyboard, from schematic to working firmware.
- Learn how to implement the USB HID protocol on a bare STM32 chip.
- Build a complete, real embedded systems project end-to-end, using the STM32 ecosystem for the first time.

The end result is meant to be a keyboard used in daily life — for regular typing, programming, and casual gaming (not competitive/FPS-focused) — not just a proof of concept left unused after completion. It will use hot-swappable switch sockets, so switches can be replaced at any time without re-soldering.

This repository is intended as a reference for anyone building their own STM32-based keyboard, or looking to reuse the firmware on the same MCU. It assumes basic embedded systems knowledge (the level of someone currently studying embedded systems) but explains project-specific decisions along the way.

---

## Roadmap

The current stage is shown in **bold**.

1. Defined the project concept: a matrix keyboard with firmware exposing it as a USB HID device.
2. Decided to first implement the full concept on a smaller Numpad, since the schematic and firmware logic are identical to a full keyboard, just with fewer keys — this avoids wasting time on a large matrix before the core design is proven.
3. Designed the Numpad schematic (power supply, MCU decoupling, crystal oscillator, USB Type-C connector, UART programming header, BOOT0 jumper, reset circuit, button matrix with diodes).
4. Designed the Numpad perfboard layout (DIY Layout Creator) to build a hardware prototype.
5. **Developing the Numpad firmware on the perfboard prototype (matrix scanning, then USB HID communication).**
6. Once the firmware is working reliably, design and order the Numpad PCB.
7. Extensively test the Numpad PCB prototype to catch any hardware or firmware issues before scaling up.
8. Design the full mechanical keyboard schematic.
9. Design the full mechanical keyboard PCB.
10. Scale the firmware from the Numpad to the full keyboard.
11. Order the full keyboard PCB.
12. Final assembly: case, keycaps, and switches.

---

## Project Structure
 
<pre>
STM32-Mechanical-Keyboard/
└── STM32-Num-Pad/
    ├── STM32-Num-Pad-Schima/
    └── STM32-Num-Pad-Perfboard Layout/
</pre>
 
---

## License

This project is licensed under **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**.

**In short:** you are free to use, modify, and build upon this project (hardware and firmware) for any non-commercial purpose, as long as you give credit to the original author. Selling this project, or anything derived from it, for profit is not permitted.

See [LICENSE.md](LICENSE.md) for the full license text.
