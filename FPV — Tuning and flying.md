---
title: FPV — Tuning and flying
tags: [fpv, fpv/tune]
---

# FPV — Tuning and flying

#fpv/tune · Note 6 of 7 · part of [[Drones]]

## First: do not tune

Modern Betaflight defaults fly well on almost any sane 5" build. If the quad
feels bad, the cause is nearly always mechanical:

- A bent prop or a bent motor bell
- A loose motor screw
- A cracked arm
- A soft-mount that has hardened or torn
- A battery sagging under load

Check all of those before you touch a PID. Most "tuning problems" are a £2 prop.

## When tuning is actually warranted

When the quad is mechanically sound and you can reliably fly the drills from
[[FPV — Simulators]], and *then* something specific is wrong:

- **Oscillation on hard throttle** — usually a filter or motor-noise problem
- **Propwash** on descents — the classic D-term and dynamic-idle territory
- **Bounce-back** after a fast flip — D too low relative to P

## Blackbox is the only honest feedback

Guessing is slow. Log a flight and look at it:

1. Enable **blackbox** logging to onboard flash or an SD card.
2. Fly a set piece: hover, a few hard throttle punches, a couple of flips, a
   descent to trigger propwash.
3. Pull the log and open it in **PID Toolbox** or the Betaflight Blackbox Explorer.
4. Look at **gyro noise spectra** first, then **step response**.

Noise → filters and mechanics. Step response → PIDs. In that order, always: PIDs
tuned on top of a noisy craft are a tune for that noise.

## Filters and the cost of them

Every filter adds latency, and latency is what makes a quad feel disconnected.
The whole game is removing the least filtering you can get away with. If you have
low noise — good motors, balanced props, soft mounts — you can lower filtering
and the quad gets sharper. If you have noise, filtering is the only thing keeping
the motors from cooking.

## Rates

Rates are personal and not a performance setting — there is no "fast" rate.
Start around 600–700°/s max, keep the same numbers in your sim, and change them
slowly. Changing rates resets your muscle memory, so do it rarely.

## Flying: the progression

Same as the sim, then extended:

1. Hover, one spot, sixty seconds
2. Figure-of-eight, both directions
3. Orbits at constant radius
4. Dives with a smooth arrest
5. Power loops
6. Split-S, Immelmann, and then linking them into a run

The thing that separates people who look good from people who look frantic is
**throttle smoothness**, not trick vocabulary.

## Keep a log

Every flight that taught you something is worth a line: pack, conditions, what
broke, what you changed. That log is the single most useful note in this whole
vault after a year — see [[FPV — Claude Code in the loop]] for keeping it without
it becoming a chore.

---

← Previous: [[FPV — The first build]] · → Next: [[FPV — Claude Code in the loop]] · Series: [[Drones]]
