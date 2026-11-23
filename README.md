# Reel safe zones

A drag-and-drop checker for Instagram Reel safe zones, in the C&C style.

**Open it:** https://ronanheal.github.io/reel-safe-zones/

Drag images or videos (straight from Dropbox in Finder) onto the page, or paste a Dropbox share link (⌘V anywhere, or the link box). File links need Dropbox sharing set to "Anyone with the link". **Folder links** work too: the first time, a Dropbox sign-in window opens (once per browser), then every image and video in the folder (and up to two levels of subfolders) is listed. Each file downloads when you open it, so Save frame works for those as well. **Disconnect** under the link box signs out. Each file gets:

- the red safe-zone overlay on top (Zones / Outline / Off, adjustable opacity)
- a 9:16 check, with a low-resolution warning under 1080 × 1920
- a player for video: scrub, frame-step, mute, ½× and ¼× speed
- a warning for videos over 3 minutes
- **Save frame**: downloads the current frame with the overlay as a PNG (dropped files only)
- **Copy check link** (Dropbox links): a link that opens the checker with that file loaded

When adding several files at once (a folder, a multi-file drop, the Dropbox picker or a Dropbox folder link), files whose **name** says another size, like `16x9`, `4x5`, `1x1` or `1920x1080`, are skipped automatically; a folder name counts too (e.g. `16x9 cutdowns/`). Files with no size in the name are added and marked **No spec**. A single file added on its own is always added.

You can also drop a whole folder, use **Select a folder**, or click **Choose from Dropbox** to pick files (several at once) straight from Dropbox. The picker uses the Dropbox app "C&C Reel Safe Zones" (app key in `index.html`; allowed domain `ronanheal.github.io`). Overlay, opacity, mute and speed are remembered in each browser.

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

## Dropbox app settings

App "C&C Reel Safe Zones", key `tymn65ngvtkr7i8`.

- Chooser domain: `ronanheal.github.io`
- Redirect URI: `https://ronanheal.github.io/reel-safe-zones/`
- Permissions: `sharing.read`, `files.metadata.read`, `files.content.read`

Sign-in uses OAuth with PKCE, so there is no app secret in the page. Tokens are kept in each person's browser only.
