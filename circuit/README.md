# Circuit / Electrical Notes

## Power Chain

Stepper motor (AC output) → Bridge rectifier (AC→DC) → Blocking diode (prevents
backflow) → Smoothing capacitor, wired in parallel (smooths DC before regulation) →
Buck converter (voltage regulation) → Portable USB battery bank → Phone charging

## Components

- **Bridge rectifier** — converts the stepper motor's AC output to DC
- **Blocking diode** — stops current from flowing back on itself
- **Smoothing capacitor** — wired in parallel via a T-joint; reduces strain on the buck
  converter and produces a cleaner signal when RPM (and therefore input current) isn't
  constant
- **Buck converter** — has a built-in voltmeter/display; regulates output for USB
  charging
- **Portable USB battery bank** — final energy storage, used to charge a phone

## Assembly Notes

- Wires were soldered to the bridge rectifier by wrapping through one hole and back out
  the top hole, stripping enough wire to twist the doubled-over section before
  soldering — gives a more stable joint than a single unwrapped pass
- Switching to a flat soldering iron tip made a big difference in joint quality
- Continuity was checked with a multimeter after each solder joint
- The smoothing capacitor's T-joint: twist the two meeting wires together, lay the
  capacitor lead across the top, solder the whole joint at once

## Results

- With everything wired into the buck converter, its built-in voltmeter lit up and
  showed current
- Motor produced ~4V when spun manually fast enough to light the display

## To Do

- [ ] Add a labeled wiring diagram (hand-drawn or photographed layout)
- [ ] Log rectifier, diode, capacitor, and buck converter part numbers/specs
- [ ] Note battery bank input voltage/current requirements
