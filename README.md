# NE555 Astable Timer — PCB Design Portfolio Project

> **Project type:** Original circuit design and PCB layout exercise (not a physical-PCB reverse-engineering project).  
> **EDA tool:** EasyEDA Standard  
> **Board approach:** Single-sided through-hole PCB  
> **Current status:** Schematic, BOM and Gerber exports collected; physical prototype has not yet been fabricated or tested.

## Overview

This project documents an NE555 timer configured as an astable oscillator. The output is intended to drive a green indicator LED through a current-limiting resistor. The design is powered from a nominal 5 V DC input.

The project is suitable as an introductory ECE/EEE portfolio example because it demonstrates schematic capture, through-hole footprint assignment, PCB placement, single-layer routing, DRC checking, BOM export and Gerber generation.

## Design specifications

| Item | Design value |
|---|---|
| Timer IC | NE555N, DIP-8 |
| Supply | 5 V DC nominal |
| RA (R1) | 1 kΩ |
| RB (R2) | 10 kΩ |
| LED resistor (R3) | 220 Ω |
| Timing capacitor (C2) | 100 µF electrolytic |
| Control-pin capacitor (C1) | 10 nF |
| Indicator | Green through-hole LED |
| PCB | Single-sided, through-hole |

## Expected operation (calculated)

Using the standard approximate NE555 astable equations:

- Frequency: `f ≈ 1.44 / ((RA + 2 RB) C)`
- High time: `tHIGH ≈ 0.693 (RA + RB) C`
- Low time: `tLOW ≈ 0.693 RB C`

For RA = 1 kΩ, RB = 10 kΩ and C = 100 µF:

- Expected frequency: approximately **0.686 Hz**
- Expected period: approximately **1.46 s**
- Expected output high time: approximately **0.762 s**
- Expected output low time: approximately **0.693 s**
- Approximate duty cycle: **52.4%**

These are idealized calculations; actual timing depends on component tolerances and the selected NE555 device.

## Circuit connections

See [`documentation/Connections.md`](documentation/Connections.md) for the pin-by-pin connection reference. Check the EasyEDA schematic against this table before fabrication.

## Repository contents

- `schematic/NE555_Schematic.pdf` — exported schematic PDF.
- `pcb/Gerber_Files_EasyEDA_Export.zip` — Gerber and drill export from EasyEDA.
- `bom/BOM.csv` — normalized UTF-8 BOM for viewing and editing.
- `bom/BOM_EasyEDA_Original_Export.csv` — original EasyEDA BOM export.
- `images/PCB_3D_View.png` — 3D PCB render supplied during design review.
- `documentation/` — calculations, connections and fabrication checklist.

## Design review and limitations

The designer reported **0 DRC errors** and **0 unrouted connections** in EasyEDA. Those are CAD checks, not proof that the assembled circuit works.

Before ordering a board, independently verify:

1. NE555 DIP-8 footprint pad numbering and pin-1 orientation.
2. C2 electrolytic polarity and its actual radial footprint diameter/lead spacing. The exported BOM shows a `CAP-D3.0xF1.5` footprint; confirm that this matches the exact capacitor being purchased.
3. H1 connector pin assignment (+5 V and GND) and polarity marking on silkscreen.
4. LED anode/cathode orientation and R3 series connection.
5. Gerber layers, board outline dimensions, drill file and single-sided copper arrangement in a Gerber viewer.
6. Clearance, copper-to-edge spacing and manufacturer minimums.

Do not describe the board as manufactured or tested until a physical prototype has been assembled and measured.

## Skills demonstrated

- NE555 astable circuit design
- EasyEDA schematic capture
- Through-hole footprint selection
- Single-sided PCB placement and routing
- Design Rule Check (DRC)
- BOM, schematic PDF and Gerber export
- Engineering documentation

## Suggested future work

- Fabricate a prototype after the checks above.
- Measure output frequency and duty cycle with an oscilloscope or frequency counter.
- Compare measured timing with the calculated value.
- Add clear +5 V/GND polarity markings and a project revision history.

## Author

Add your preferred public display name, institution (if desired), and GitHub profile link here. Do not publish private contact details.
