# Reel safe zones

A drag-and-drop checker for Instagram Reel safe zones, in the C&C style.

**Open it:** https://ronanheal.github.io/reel-safe-zones/

Drag images or videos (straight from Dropbox in Finder) onto the page, or paste a Dropbox share link (⌘V anywhere, or the link box). Links need Dropbox sharing set to "Anyone with the link"; folder links won't work, so copy the link for a single file. Each file gets:

- the red safe-zone overlay on top (Zones / Outline / Off, adjustable opacity)
- a 9:16 check, with a low-resolution warning under 1080 × 1920
- a player for video: scrub, frame-step, mute, ½× and ¼× speed
- a warning for videos over 3 minutes
- **Save frame**: downloads the current frame with the overlay as a PNG (dropped files only)
- **Copy check link** (Dropbox links): a link that opens the checker with that file loaded

You can also drop a whole folder, or use **Select a folder**. Overlay, opacity, mute and speed are remembered in each browser.

Files are read by the browser and are never uploaded anywhere.

## Keep clear at 1080 × 1920

| Area | Size |
| --- | --- |
| Top | 227 px |
| Bottom | 324 px |
| Sides | 50 px |
| Right, lower half | 190 px |

## Updating

It's one static page (`index.html`) served by GitHub Pages. Edit it, push to `main`, and the live link updates within a minute or two.
