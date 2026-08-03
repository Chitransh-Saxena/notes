---
title: The capo
aliases: [Guitar — The capo]
tags: [music, music/capo]
---

# The capo

#music/capo · Note 6 of 9 · part of [[Guitar]]

> **A capo is a movable nut.**
>
> That is the whole device. Everything below is a consequence of it.

## The physics

A stretched string's fundamental frequency is

```
f = (1 / 2L) · √(T / μ)
```

- **L** — the vibrating length
- **T** — the tension
- **μ** — mass per unit length

A capo changes **only L**. The string is the same string at the same tension, so
tension and mass drop out and what is left is

```
f ∝ 1 / L
```

**Halve the length, double the frequency.** That is why the 12th fret — exactly
halfway along the string — is an octave. Not by convention: by measurement.

### Where the frets are

Guitars use **equal temperament**: the octave is split into twelve equal
*ratios*, not twelve equal distances. One semitone is

```
2^(1/12) ≈ 1.059463
```

To raise the pitch one semitone, the length must shrink by the inverse:

```
L′ = L / 1.059463 ≈ 0.943874 · L
```

So fret **n** sits at

```
distance from nut = L · (1 − 2^(−n/12))
```

Fret 1 lands at `L × 0.056126`, or **L / 17.817** — the old luthier's "rule of
18". Each fret is that same fraction of the *remaining* length, which is why
frets crowd together as you climb. The spacing is geometric, and it has to be,
because pitch is.

### A worked example

The open 5th string is **A = 110 Hz**.

| Capo | Length | Frequency | Note |
| --- | --- | --- | --- |
| none | L | 110 Hz | A |
| fret 2 | 0.891 L | 110 × 2^(2/12) = **123.5 Hz** | B |
| fret 5 | 0.749 L | 110 × 2^(5/12) = **146.8 Hz** | D |
| fret 12 | 0.500 L | 110 × 2 = **220 Hz** | A, one octave up |

## What it does musically

A capo at fret **n** raises **every string by n semitones**. Standard tuning
becomes:

| Capo | 6th | 5th | 4th | 3rd | 2nd | 1st |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | E | A | D | G | B | E |
| 2 | F♯ | B | E | A | C♯ | F♯ |
| 3 | G | C | F | B♭ | D | G |
| 5 | A | D | G | C | E | A |
| 7 | B | E | A | D | F♯ | B |

Your **shapes do not change**. The chord they *sound* moves up n semitones:

| Capo | C shape | G shape | D shape | A shape | E shape | Am | Em |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | C | G | D | A | E | Am | Em |
| 1 | C♯ | G♯ | D♯ | A♯ | F | A♯m | Fm |
| 2 | **D** | **A** | **E** | **B** | **F♯** | **Bm** | **F♯m** |
| 3 | D♯ | A♯ | F | C | G | Cm | Gm |
| 4 | E | B | F♯ | C♯ | G♯ | C♯m | G♯m |
| 5 | **F** | **C** | **G** | **D** | **A** | **Dm** | **Am** |
| 7 | G | D | A | E | B | Em | Bm |

Read it as arithmetic: **sounding chord = shape + capo frets**, counted in
semitones. Nothing else to remember.

## In sargam: Sa moves, and nothing else does

[[Sargam and the scale]] makes the point that Sa is not a pitch, it is
*home* — and that every fret pattern is a set of offsets from wherever you put
it. A capo is that idea made physical.

Play open C shapes and **Sa = C**. Clamp a capo at fret 2 and **Sa = D**. The
offsets `0 2 4 5 7 9 11 12` are untouched. Re is still two frets above Sa; Ga is
still four; the Ga→Ma and Ni→Sa′ half steps land exactly where they did.

The capo has not changed the music's *relationships* at all. It has only chosen a
different Sa. A singer who cannot reach the top of a song in C is not asking for
different music — they are asking for a different Sa, and this is the two-second
way to give them one.

## Why bother, when barre chords exist

A barre chord transposes too, so the capo is not about avoiding work. It is
about **open strings**.

When you barre, every string is stopped by your finger. With a capo, every
string is stopped by a bar of metal or rubber *and the strings above it ring
open*. Those open strings:

- sustain far longer than a fretted note
- vibrate sympathetically when other notes are struck
- carry a different overtone balance — brighter, with more upper partials

That is a timbre you cannot get from a barre chord, in any key. Playing in E♭
with a capo at 3 and G shapes sounds like a G-shaped guitar; playing E♭ with
barre chords sounds like a barred guitar. Both are E♭. They are not the same
sound.

Three good reasons, then:

1. **Match a voice** without relearning anything.
2. **Keep the open-string ring** in keys that would otherwise demand barres.
3. **Two guitars, one song** — capo one of them and the same chords become two
   different voicings, which is most of what makes two acoustic guitars sound
   large.

## What it does not do

- It does not change intervals, or the key's internal relationships.
- It does not transpose *you*. If you are reading a chart in F and put a capo at
  1 playing E shapes, you are still responsible for knowing it sounds in F.
- It does not fix a tuning problem. It usually reveals one.

## Practical, and one more piece of physics

**Place it just behind the fret** — as close as you can without sitting on top of
the fret wire. On the fret itself it buzzes; too far back and it pulls the string
sharp.

**Use the least pressure that stops the buzz.** Squeezing does not just clamp the
string, it *stretches* it — which raises **T** in the equation above, which
raises the pitch. An over-tightened capo sharpens the strings, and it sharpens
the thin ones most. This is the single most common reason a capo'd guitar sounds
out of tune when the open guitar was fine.

**Retune after fitting it**, especially above the 5th fret, where small errors in
placement are a larger fraction of the remaining string length.

**Partial capos** clamp only some strings — five, or three — which is a way of
producing an open tuning without retuning anything. A different note.

---

← Previous: [[Beyond the triad]] · → Next: [[Rhythm and tempo]] · Series: [[Guitar]]
