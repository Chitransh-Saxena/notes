---
title: The first build
aliases: [FPV — The first build]
tags: [fpv, fpv/build]
---

# The first build

#fpv/build · Note 5 of 7 · part of [[Drones]]

A 5" freestyle build, which is the standard first build for good reasons: parts
are cheap, everything is documented, and it flies well enough to grow into.

## The parts list

| Part | Notes |
| --- | --- |
| Frame | 5", 5–6mm arms. Replaceable single arms, not a unibody |
| Stack | FC + 4-in-1 ESC, 30×30mm. 45–60A is plenty for 4S/6S |
| Motors | 2207, ~1800–2000KV for 6S, ~2400–2550KV for 4S |
| Camera | Match the video system — analogue or digital |
| VTX | Analogue: 400–800mW switchable. Digital: comes as a set with the camera |
| Receiver | ELRS, matching your radio from [[What to buy]] |
| Props | 5×4.3×3 or similar. Buy ten sets |
| Straps, foam, zip ties | The build is 10% electronics and 90% strain relief |

## The tools

- **Temperature-controlled soldering iron**, 60W+. A pencil iron from a hardware
  shop will not heat a battery pad and you will spend an hour cold-soldering it.
  A TS100/TS101 or a Pinecil is inexpensive and correct.
- **Leaded solder**, 60/40 or 63/37. Lead-free is harder for no benefit here.
- **Flux.** Not optional. Most bad joints are a flux problem.
- **Helping hands**, side cutters, hex drivers (1.5/2.0/2.5mm), tweezers.
- **Multimeter** with a continuity beep.
- **Smoke stopper** for first power-up.

## Order of assembly

Doing this in the wrong order means desoldering things later.

1. **Tin everything first** — pads on the ESC, wire ends. Never solder untinned.
2. **Motors to arms**, then route the wires. Cut them to length now, while you
   can still reach the pads.
3. **Motors to ESC.** Order does not matter electrically — you fix direction in
   software later.
4. **Capacitor across the battery pads.** Low-ESR, 35V, 470–1000µF. It protects
   everything and cleans up video noise. Do not skip it.
5. **XT60 to the battery pads.** Get polarity right. Check it twice, then check
   with the multimeter.
6. **Stack in**, with the FC on soft mounts if the frame supports it.
7. **VTX and camera.** Keep the VTX antenna clear of carbon.
8. **Receiver**, antennas out at 90° to each other.
9. **Continuity check.** Battery + to − should not beep. If it does, stop.
10. **Smoke stopper, then power.** Only then, a real battery.

## Betaflight, first flight

Order matters here too:

1. **Ports** — set UART for the receiver and any telemetry.
2. **Receiver** — protocol, then bind, then confirm all channels move.
3. **Modes** — arm switch first. Set a **failsafe** and test it by turning the
   radio off with props removed.
4. **Motors tab, props off.** Check direction and order. Fix in software.
5. **Rates** — start modest, around 600–700°/s, matching your sim
   ([[Simulators]]).
6. **Do not tune anything.** Stock Betaflight tunes are genuinely good.
   [[Tuning and flying]] explains when that stops being true.

## The mistakes everyone makes once

- **Reversed polarity on the XT60.** Instantly fatal to the stack. This is what
  the smoke stopper is for.
- **Cold joints** — dull, blobby, and they fail in flight rather than on the bench.
- **Unsecured wires near props.** A prop finds any loose wire immediately.
- **Props on the wrong way.** They are marked; the quad will flip and you will
  blame the tune.
- **Arming with props on, indoors, "just to check".** Do not.

> [!danger] Batteries
> LiPos are the genuinely dangerous part of this hobby, not the props. Never
> charge unattended, never charge a puffed pack, never leave one at full charge
> for weeks. Storage charge is ~3.8V per cell.

---

← Previous: [[What to buy]] · → Next: [[Tuning and flying]] · Series: [[Drones]]
