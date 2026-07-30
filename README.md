# Savonius-Style Vertical Axis Wind Turbine (VAWT)

**Author:** Brendan Spires
**Course:** Engr 1201 — Final Project

## Objective

Construct a Savonius-style Vertical Axis Wind Turbine (VAWT) with a structural footprint
of less than 3 ft³, capable of generating stable current in low-to-turbulent wind
conditions. Energy is stored in a portable battery bank and used to charge a phone.
Constraints: minimal tools, low cost.

## Project Status

**Phase:** V1 complete (Engr 1201 final project) — did not meet functional objective.
V2 planning in progress.

See [`docs/engineering-log.md`](docs/engineering-log.md) for the full build history and
[`docs/reflection.md`](docs/reflection.md) for root-cause analysis of what didn't work
and what's changing for the next attempt.

## Design Overview

- 3-gallon bucket enclosure (pivoted from a small junction box once the 3ft dowel rod
  wouldn't stay upright in it) housing electronics, shielded from weather; the lid
  doubles as an upper support point for the central pole
- PVC support structure holding a central ½" wooden dowel rod — chosen over wood/glass
  supports specifically to cut down drivetrain friction
- Timing pulley + belt system transferring rotation from the dowel rod to a stepper
  motor
- Half-cylinder rotors (Savonius scoops), ultimately improvised from cut plastic bottles
  after no affordable rigid material could be sourced in time
- Bridge rectifier → blocking diode → smoothing capacitor → buck converter chain,
  charging a portable USB power bank

Hand-drawn design diagrams are in [`docs/diagrams`](docs/diagrams). Full build narrative
with dates is in [`docs/engineering-log.md`](docs/engineering-log.md).

## Repository Structure

```
docs/            Engineering log, reflection, hand-drawn diagrams
media/photos/    Build photos
media/videos/    Build videos / links
circuit/         Wiring diagrams, component notes (rectifier, buck converter, etc.)
data/            Test data (voltage, current, RPM, wind speed)
presentation/    Slides / write-ups for presenting the project
```

## Key Results (V1)

**Successes:**
- Working understanding of AC-to-DC rectification and current smoothing
- Soldering and multimeter/continuity-testing practice
- Motor produced a measurable ~4V when spun fast enough by hand

**Failures:**
- Rotors improvised from cut plastic bottles — too flexible to catch meaningful wind
- Enclosure lid compressed the PVC supports and dowel rod, drastically increasing
  starting torque needed
- Combined friction meant ambient wind was never enough to turn the rotor — no
  self-sustained electricity generation
- Belt/pulley system needed constant high tension or it would slip

Full writeup: [`docs/final-report.md`](docs/final-report.md)

## Planned Changes for V2

- Replace belt/pulley with interlocking gears (less slippage, more mechanical advantage)
- 3D-printed scoops locked 120° apart on a ½" bore (consistent, rigid wind capture)
- Rectangular housing instead of cylindrical for stability and easier mounting
