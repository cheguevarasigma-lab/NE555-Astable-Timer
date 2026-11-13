# Fabrication Readiness Checklist

- [ ] Confirm U1 is NE555N with the correct DIP-8 pad numbering and pin-1 marker.
- [ ] Confirm C2 is a polarized 100 µF electrolytic; verify polarity and real component lead spacing/body diameter.
- [ ] Confirm C1 is 10 nF and correctly connected from pin 5 to GND.
- [ ] Confirm H1 pad-to-net assignment and add visible +5 V/GND silkscreen labels.
- [ ] Confirm LED1 anode/cathode and R3 series path.
- [ ] Confirm all copper tracks are on the intended single copper side; no vias are required.
- [ ] Open the Gerber ZIP in a Gerber viewer and inspect copper, mask, silkscreen, outline and drill alignment.
- [ ] Confirm board outline is closed and dimensions are correct.
- [ ] Confirm manufacturer minimum track width, clearance, drill and edge clearance.
- [ ] Re-run DRC and confirm zero unrouted connections.
- [ ] Fabricate only after all checks are complete.
- [ ] After assembly, test with a current-limited 5 V supply and measure the oscillation frequency.
