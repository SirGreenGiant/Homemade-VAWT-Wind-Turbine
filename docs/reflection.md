# Reflection — V1

| Mistake | Root Cause | Fix | Lesson Learned |
|---|---|---|---|
| Lost early design notes/sourcing | Doc didn't save, no backup | Keep this repo as the single source of truth going forward — commit often | Don't rely on one unsaved doc for project notes; commit early, commit often |
| Wrong-size gear/pulley ordered | Didn't verify fit against the actual stepper motor shaft before ordering | Measure and confirm bore/shaft sizes against physical parts before ordering | Measure twice on mechanical fit — a spec sheet number isn't the same as test-fitting the part |
| Rotors didn't catch wind | Couldn't source a rigid, affordable scoop material in time; ended up with cut plastic bottles | 3D-print rigid scoops, 120° spaced, ½" bore | Don't substitute a structural part with whatever's on hand — geometry and rigidity matter as much as shape |
| Central rod wouldn't turn in ambient wind | Enclosure lid compressed PVC supports onto the dowel rod, raising friction; belt tension fix (rod pressed against a metal lid) added even more resistance | Rectangular housing with independently mounted supports; revisit tensioning method | Enclosure design isn't just weatherproofing — it can silently load the drivetrain |
| Belt slipped under abrupt rotation | Timing belt requires constant high tension to grip pulley teeth | Switch to interlocking gear train | Friction-based transmission (belts) is fragile under variable, low-torque input; positive-engagement transmission (gears) is more forgiving |
| No self-sustained power generation | Combination of the above — cumulative friction (compressed PVC + belt tension fix + improvised rotors) exceeded any torque available wind could provide | Address all of the above simultaneously in V2 | System-level failures often stack — fixing one bottleneck without the others still won't work |

**Overall takeaway:** the project didn't meet its functional objective, but every failure
mode is diagnosed and has a specific fix queued for V2. The electronics side (rectification,
blocking diode, smoothing capacitor, buck converter) worked as intended — the mechanical
drivetrain and friction management is where V2 effort should concentrate. Also came away
with a new interest in ESP32-based projects as a possible next build.
