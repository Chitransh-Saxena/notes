---
title: Obsidiary
tags: [project]
---

# Obsidiary

An open-source publisher for Obsidian vaults. This site runs on it.

- Source: <https://github.com/Chitransh-Saxena/obsidiary>
- Docs and live demo: the project site

## Why I built it

Obsidian Publish is $10 a month. Quartz is free and good, but two things bothered
me: your notes have to live inside its source tree, and upgrading it usually
means resolving a merge in your own content.

So: the engine is an npm package, and the vault is just a repository it reads.
Upgrading is `npm update`. There is nothing of mine in your notes folder.

## What it does

Wikilinks with Obsidian's actual resolution rules, transclusion that inlines real
content, callouts, backlinks with context, a graph, full-text search, and
`.canvas` files rendered as pages.

It also reads any public vault in the browser with no build at all, which turned
out to be the most useful part for reading other people's notes.

See also [[Engineering]].
