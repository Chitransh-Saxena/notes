---
title: Notes
---

# Notes

Public working notes — things I'm building, learning, or trying to understand
properly. Written in Obsidian, published with
[Obsidiary](https://github.com/Chitransh-Saxena/obsidiary).

This is a garden, not a blog. Notes here get edited, contradicted and rewritten.
Nothing is finished.

## Areas

| Folder | | |
| --- | --- | --- |
| `engineering/` | [[Engineering]] | systems, tools, and the things I keep re-deriving |
| `fpv/` | [[Drones]] | builds, tuning, flying — a seven-part series |
| `photography/` | [[Photography]] | exposure, low light, night sky — a seven-part series |
| `music/` | [[Guitar]] | songs, theory, practice |
| `reading/` | [[Reading]] | books and what stuck |
| `boards/` | [[FPV build map]] | a canvas, rendered as a page |

## How this is organised

One folder per area, each holding a hub note that points at the rest. Series are
numbered and linked head-to-tail, so they can be read straight through or dipped
into. Tags cut across the folders — `#fpv/build`, `#photo/lowlight` — and every
one of them has its own page.

Attachments live in `attachments/`. See
[[Adding photos to these notes]] for how images are served.

## How this works

The repository behind this site *is* the vault. There's no export step and no
CMS: I write in Obsidian, push, and this rebuilds. Every page links back to the
markdown file that made it, and carries the date of its last commit.

If you want the same thing, the whole engine is open source and the setup takes
about five minutes.
