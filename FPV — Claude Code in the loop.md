---
title: FPV — Claude Code in the loop
tags: [fpv, fpv/tools, claude-code]
---

# FPV — Claude Code in the loop

#fpv/tools · Note 7 of 7 · part of [[Drones]]

Where an agent actually earns its keep in this hobby, and where it does not.

## Where it genuinely helps

**Blackbox analysis.** Export a log to CSV and have it plot gyro spectra, compare
two flights before and after a filter change, and tell you which axis is noisy.
This is exactly the sort of tedious numeric work that is quick to describe and
slow to do. Pairs with [[FPV — Tuning and flying]].

**Betaflight CLI diffs, versioned.** `diff all` after every change, saved into
this vault as a dated file. Then ask for the diff *between* two of them. Six
months later, "what did I change when it started oscillating" becomes answerable
instead of a memory test.

**Bills of materials.** Give it the parts list from [[FPV — The first build]] and
have it produce a table with weights and prices, total AUW, and a hover-thrust
sanity check. Then keep that table in the vault and embed it into every build note
that uses the same parts — write once, reuse.

**Weight and thrust budgets.** Thrust-to-weight from motor thrust-test data, with
the arithmetic done properly rather than in your head at 1am.

**Battery cycle logs.** A note per pack, cycles appended, internal resistance
tracked over time. It will tell you a pack is dying before it dumps you out of
the sky.

**Parametric CAD dimensions.** Keep the numbers from [[FPV — CAD and simulation]]
in a note rather than only inside the model, so the mount and the notes cannot
disagree.

**The wiring diagram.** A `.canvas` file is just JSON — it can be generated. See
[[FPV build map]] for what a canvas looks like once rendered.

**These notes.** Structure, cross-links, and consistent tags across a growing
series is exactly the work that decays when done by hand.

## Where it does not help

> [!warning] Verify every specification
> An agent will state a motor's KV, a battery's C rating or an ESC's current
> limit with complete confidence and no source. **Check the vendor page.** Getting
> this wrong is not a typo, it is a fire.

- **It cannot tune your quad.** It has never felt propwash. It can read a log; it
  cannot tell you whether the quad feels sharp.
- **It cannot judge a solder joint.** Send it a photo and it will say something
  agreeable. Look at the joint yourself.
- **It should not be trusted on airspace rules.** These are jurisdictional and
  they change. Read the primary source.

## The pattern that works

Keep the *artifacts* in the vault — CLI diffs, BOMs, logs, cycle counts — and use
the agent to transform and query them. The vault is the memory; the agent is the
processing. Neither is much use without the other, and only one of them is
still there in five years.

---

← Previous: [[FPV — Tuning and flying]] · Series: [[Drones]] · Board: [[FPV build map]]
