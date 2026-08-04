---
title: Adding photos to these notes
aliases: [Photo — Adding photos to these notes]
tags: [photo, photo/workflow, obsidiary]
---

# Adding photos to these notes

#photo/workflow · Note 7 of 7 · part of [[Photography]]

How images actually work in this vault, because this repository is published in
a slightly unusual way and it changes the answer.

## Where they go

`attachments/` at the vault root. Obsidian can be told to put them there
automatically: **Settings → Files & Links → Default location for new
attachments → In the folder specified below → `attachments`**.

Then the ordinary Obsidian syntax works:

```markdown
![[bangalore-rooftop.jpg]]
![[bangalore-rooftop.jpg|600]]
  ← 600px wide
![[bangalore-rooftop.jpg|600x400]]
  ← both dimensions
```

Here is one, proving the whole path end to end:

![[test-card.png|420]]

## The unusual bit

This repository holds **only markdown and images** — no site, no build. The site
at `notes.pulsar-projects.org` lives elsewhere and reads this repo over the
GitHub API. Which means:

> **Images are never copied into the site.** The published page points straight
> at `raw.githubusercontent.com`, where the file already is.

Consequences worth knowing:

- **A vault full of photographs does not bloat the deploy.** The site stays a few
  hundred kilobytes no matter how many images are in here.
- **Filenames are case-sensitive** on the raw host. `Photo.JPG` and `photo.jpg`
  are different files. Obsidian on macOS is more forgiving than the web will be.
- **Spaces are fine** — they get URL-encoded — but hyphens age better.
- A pushed image is live as soon as the site rebuilds; no upload step anywhere.

## Sizing, before you commit

Git keeps every version of a binary file forever. A repository of 40MB RAWs
becomes unpleasant to clone within a year.

- **Long edge 2000px** is plenty for any screen
- **JPEG quality ~80**, which lands most photographs under 1MB
- **Never commit RAW files.** Keep those locally or in cloud storage; this vault
  holds the notes and the finished exports
- WebP or AVIF if size matters more than universal compatibility — both render

## The privacy trap

> [!danger] EXIF is published verbatim
> Because the file is served exactly as committed, **all of its metadata comes
> with it** — including GPS coordinates. A photo taken at home, published here,
> tells anyone who downloads it precisely where you live.
>
> Strip location before committing. On macOS, Preview → Tools → Show Inspector →
> GPS → *Remove Location Info*. Or in bulk:
> ```bash
> exiftool -gps:all= -xmp:geotag= \
>   attachments/*.jpg
> ```
> Camera model and settings are harmless and worth keeping. Location is not.

## Alt text

`![[photo.jpg]]` gives no alt text. Where an image carries meaning rather than
decoration, use the markdown form instead:

```markdown
![Milky Way](attachments/milky-way.jpg)
```

## What renders

Images, video (`mp4`, `webm`), audio (`mp3`, `m4a`) and PDFs all embed with the
same `![[...]]` syntax. So a build video or a voice note works exactly like a
photograph.

---

← Previous: [[Night sky]] · Series: [[Photography]]
