# NE555 Astable Timer — Calculations

## Given values

- Supply voltage: 5 V DC nominal
- RA = R1 = 1 kΩ
- RB = R2 = 10 kΩ
- C = C2 = 100 µF = 0.0001 F

C1 = 10 nF is the control-pin bypass capacitor; it is not used in the astable timing calculation.

## Frequency

`f ≈ 1.44 / ((RA + 2 RB) C)`

`f ≈ 1.44 / ((1000 + 2 × 10000) × 0.0001)`

`f ≈ 0.686 Hz`

## Timing intervals

`tHIGH ≈ 0.693 (RA + RB) C ≈ 0.762 s`

`tLOW ≈ 0.693 RB C ≈ 0.693 s`

`T ≈ tHIGH + tLOW ≈ 1.455 s`

## Duty cycle

`D ≈ (RA + RB) / (RA + 2 RB) × 100%`

`D ≈ 11 / 21 × 100% ≈ 52.4%`

These are approximate ideal calculations. Real values vary with resistor/capacitor tolerance, leakage, supply conditions and the timer IC.
