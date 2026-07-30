# Engineering Log

Log format for new entries:

```
## YYYY-MM-DD — Session goal

**Materials used:**
-

**Photos:** media/photos/...
**Video:** media/videos/...

**What worked:**
-

**Problems:**
-

**Solutions / workarounds:**
-

**Next steps:**
-
```

---

## 2026-07-15 — Parts arrive, plan hits its first snags

A few weeks prior, I put together a rough plan for the turbine, built a parts list, and
ordered everything, paying close attention to sizes. Parts arrived — and immediately two
problems showed up:

- The geared piece I ordered was too small to fit over the stepper motor's rotating pin.
  Will need to send it back or repurpose it.
- The timing belts that arrived are smaller than expected, but likely workable.

**Setback:** all of my original notes, sourcing, and early design thinking were lost —
a doc didn't save. Rebuilding documentation from this point forward.

---

## 2026-07-16 — Enclosure rethink, landing on the Savonius design

**7:13 AM**

Realized PVC pipe is a cheap, modular option for the turbine's internal support
structure — no need to fill the box with wood supports like originally planned. Plan is
to draw up the design today and go to Home Depot this weekend. Also reconsidering the
"geowind" turbine design — read that it doesn't fit this use case, so researching more
conventional small-form-factor wind turbine designs instead.

**3:19 PM**

Landed on a **Savonius-style VAWT**. Also thought through a cheap material option for
the semi-cylindrical scoops — planning to check Goodwill for cheap plastic flower pots
to cut and shape, with Dollar Tree as a backup. At Home Depot: PVC pipe + pipe brackets
for mounting to the enclosure. Ordered a differently-sized timing pulley and belt
tonight to fix the fit problem from 7/15.

**9:15 PM**

Worked out a contingency plan in case the gear ratio ends up insufficient and needs to
be doubled: since the two large gears have different bore diameters, they'd need to
share a rod via a brass ¼"-to-½" plumbing adapter, joining a ¼" and ½" dowel rod cut to
length, secured with PVC so the assembly can still spin freely.

**Key concern raised:** friction between the windmill (rotor) side and the generator
side will eat into input energy. Plan to minimize this by using PVC instead of
wood-on-wood or wood-on-glass contact points, since PVC is easier to size precisely.

---

## 2026-07-20 — Missing components, enclosure redesign

Started filming and realized some components were missing. Placed one more (hopefully
final) order for:
- A **blocking diode**, to stop current from flowing back on itself
- A **smoothing capacitor**, to smooth the DC signal before the buck converter — reduces
  strain on the buck converter and gives a cleaner signal when RPM isn't constant

Also revisited the enclosure choice. Original plan was a small black-and-yellow Home
Depot junction box, but the 3ft dowel rod wouldn't stay upright in something that small.
While looking for a taller option, found cheap **3-gallon Home Depot buckets with
lids** — the lid works well as an upper support point for the central pole the fins
attach to.

**Still undecided:** rotor scoop material. Leaning toward cutting cheap plastic flower
pots in half and screwing them to the center pole — to be decided tomorrow.

**Next steps:** write the video script, draw up diagrams.

---

## 2026-07-24 — Wiring day

Components that arrived the day before finally got wired in (work delayed the start by
a day).

**Soldering:** rough going at first, but switching to a different (flat) soldering iron
tip made a big difference. Used it to solder wires to the bridge rectifier, wrapping
through one hole and back out the top, stripping enough wire to twist the doubled-over
section for a more stable joint before soldering.

Wired the current stopper (blocking diode) in and soldered the smoothing capacitor in
parallel using a T-shaped joint — twisted two meeting wires together, laid the
capacitor lead across the top, and soldered the whole joint at once.

**Success:** with everything wired into the buck converter, its built-in voltmeter lit
up and showed current.

**Problem flagged early:** the stepper motor is noticeably harder to turn by hand than
expected — flagged as a possible issue for later.

---

## 2026-07-25 — Construction day, torque problem confirmed

Started building with only a hacksaw and wire cutters on hand — cutting the bucket
plastic, PVC pipe, and wooden dowel rod was harder than expected. Used sandpaper to
clean up hacksaw cuts and to sand the dowel rod down enough to seat the timing pulley.

**Success:** the PVC support structure holding the dowel upright worked — the PVC
T-joint fits cleanly through the lid's top hole.

**Problem:** putting the lid on compresses the PVC and the dowel rod, significantly
increasing the force needed to spin it.

Got the stepper motor screwed into the bottom of the bucket and the timing belt onto
both pulleys, but the belt didn't have enough tension to grip. Fixed (for now) by
screwing a metal lid to the bucket bottom so the end of the dowel rod presses against
its edge, creating tension.

**Result:** the rod turns, the belt holds, and the voltmeter lights up. But the torque
needed to turn the assembly is far higher than expected — likely too high for the
rotor/wings alone to overcome in realistic wind. Would need something close to
tornado-level wind to self-start.

---

## 2026-07-27 — Final assembly, rotor material, wrap-up

Couldn't find an affordable rotor scoop material anywhere, so ended up cutting up
plastic bottles on hand and attaching them to the center dowel. Noted that a 3D printer
would have solved this cleanly if attempted again.

**Result:** the turbine does not spin under available wind. Combined friction from the
compressed PVC/dowel assembly and belt tension setup outweighs any torque the improvised
plastic-bottle scoops can generate.

**Overall:** project didn't meet its functional goal, but a lot was learned hands-on
about soldering, circuit assembly, and mechanical troubleshooting. Also got interested
in ESP32 projects along the way — likely the next thing to build with the new soldering
iron and renewed interest in electronics.
