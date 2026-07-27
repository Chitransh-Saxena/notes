---
title: FPV — CAD and simulation
tags: [fpv, fpv/cad, cad]
---

# FPV — CAD and simulation

#fpv/cad · Note 3 of 7 · part of [[Drones]]

Two different things get called "simulation" in this hobby and it is worth
separating them before choosing a tool:

- **Flight simulation** — learning to fly. That is [[FPV — Simulators]], and the
  answer is a game, not a CAD package.
- **Design simulation** — will this part survive a crash. That is CAD and FEA,
  and it is what this note is about.

## On AutoCAD specifically

Worth being straight about it: **AutoCAD is not the right tool here.** It is
drafting software, strongest in 2D and in architectural/engineering documentation,
and it is not free. It has a free one-year *student* licence, which is legitimate
if you qualify, but even then it is an awkward fit for organic 3D parts like a
camera mount.

If you want to model drone parts, these are better and genuinely free:

| Tool | Cost | Good for |
| --- | --- | --- |
| **FreeCAD** | Free, open source | Parametric parts, and it has an FEM workbench for stress analysis |
| **Onshape** | Free for public documents | Browser-based parametric CAD, excellent constraints, nothing to install |
| **Fusion 360** | Free personal licence | The most pleasant of the three; watch the personal-use restrictions |
| **Tinkercad** | Free | Ten minutes to a printable antenna mount. Not parametric, but fast |
| **Blender** | Free, open source | Organic shapes and renders; not a CAD tool, don't use it for tolerances |

**Onshape** is the one I would start with — no install, no licence anxiety, and
the constraint solver teaches you to model properly.

## What is actually worth modelling

Not the frame. Carbon frames are cheap, tested, and you cannot cut carbon at home
safely without proper extraction — the dust is genuinely hazardous.

What you print:

- **TPU camera mounts and guards** — the part that dies most often
- **Antenna mounts** — geometry matters here, keep the antenna clear of carbon
- **Battery pads and straps' anti-slip**
- **GoPro / naked-cam mounts** at whatever angle you actually fly
- **Motor soft-mounts** and washers

Print TPU (95A) for anything that should absorb a crash, PETG for rigid brackets.
PLA is fine for prototypes and useless in a hot car.

## Stress analysis, honestly

You can run FEA on an arm in **FreeCAD's FEM workbench** or **SimScale's** free
community tier, and it is a good way to learn where stress concentrates — usually
at the motor mount holes and the arm root.

But: crash loads are impact loads, they are enormously variable, and modelling
them properly is real engineering. Treat FEA here as *insight*, not *proof*. The
empirical test is cheaper and more honest — fly it, crash it, see what broke.

CFD for prop wash is firmly in the "interesting, not useful" category for a
hobby build. Skip it.

## The workflow that works

1. Measure the real part with calipers. Twice.
2. Model it parametrically so the mount hole spacing is a variable, not a number.
3. Print one. Fit it. It will be wrong.
4. Change the variable, print again.

Keeping the model parametric is the whole benefit — see
[[FPV — Claude Code in the loop]] for keeping the dimensions and the build log in
one place.

---

← Previous: [[FPV — Simulators]] · → Next: [[FPV — What to buy]] · Series: [[Drones]]
