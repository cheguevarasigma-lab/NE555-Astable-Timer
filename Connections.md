# NE555 Astable Timer — Connection Reference

| NE555 pin | Name | Intended connection |
|---:|---|---|
| 1 | GND | Ground net |
| 2 | TRIG | Tied to pin 6 and timing-capacitor positive node |
| 3 | OUT | R3 (220 Ω), then LED anode; LED cathode to GND |
| 4 | RESET | +5 V |
| 5 | CONT | C1 (10 nF) to GND |
| 6 | THRES | Tied to pin 2 and timing-capacitor positive node |
| 7 | DISCH | Junction between R1 (1 kΩ) and R2 (10 kΩ) |
| 8 | VCC | +5 V |

## Timing network

- R1 (1 kΩ): +5 V to pin 7.
- R2 (10 kΩ): pin 7 to pins 2/6 node.
- C2 (100 µF electrolytic): positive to pins 2/6 node; negative to GND.

## Power connector

H1 is a 2-pin connector. Confirm its actual pad/net mapping in the PCB editor and label the connector polarity on the board. The intended nets are +5 V and GND; do not infer pin order from connector orientation alone.

## Important

This table is the intended circuit reference. Verify every net against the final EasyEDA schematic and PCB netlist before fabrication.
