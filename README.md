# Wedding Invitation — Fortuna & Atha

Digital wedding invitation for **dr. Putri Fortuna Sari & dr. Hilmy Atha Sitepu**
Online invitation (version 1) — Akad Nikah & Tasyakuran, 28 November 2026.
Watch live on Instagram Stories: [@dokteratha](https://www.instagram.com/dokteratha/) & [@dr.fortunaps](https://www.instagram.com/dr.fortunaps/).

## Files

| File | Purpose |
|------|---------|
| `index.html` | The invitation page |
| `qr.png` or `qr.jpg` | **You upload this** — QR code shown in the Wedding Gift section |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |
| `README.md` | This file |

## Publish with GitHub Pages

1. Create a new **public** repository on GitHub (e.g. `wedding-fortuna-atha`).
2. Upload `index.html`, `.nojekyll`, `README.md` and your QR image (Add file → Upload files → Commit).
   The QR file must be named exactly `qr.png` or `qr.jpg` (lowercase) and sit next to `index.html`.
   - Tip: `.nojekyll` is hidden on some computers. If you can't see it, create it on GitHub instead: Add file → Create new file → name it `.nojekyll` → commit (empty is fine).
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. After a minute or two the site is live at:
   `https://<your-username>.github.io/wedding-fortuna-atha/`

Or from a terminal:

```bash
git init
git add .
git commit -m "Wedding invitation"
git branch -M main
git remote add origin https://github.com/<your-username>/wedding-fortuna-atha.git
git push -u origin main
```

## Personalised guest links

By default the cover reads "Kepada Sahabat-sahabat kami". To address one person, add `?to=`
(spaces become `+` or `%20`):

```
https://<your-username>.github.io/wedding-fortuna-atha/?to=Budi+Santoso
```

The cover will then show "Kepada Budi Santoso". `?dear=` and `?kepada=` also work.

## Important: what still depends on soloinveet.com

This page is a saved copy of the Soloinveet invitation. The text is in `index.html`,
but these still load from `soloinveet.com`:

- Styles, fonts, couple photos, gallery, flower animations and background music

If Soloinveet removes the original page or its files, the GitHub copy will lose its
styling, images and music. To make it fully independent, download the CSS, images,
`.json` animations and `.mp3` into an `assets/` folder and change the URLs in
`index.html` to point there.

## Changes made from the original file

- All `http://` links switched to `https://` — GitHub Pages is HTTPS-only, so the
  music and flower animations would otherwise be blocked by the browser.
- Guest-name link fixed: the original script looked for "Tamu Undangan", but the
  cover text is "(Tulisnamatamu)", so `?to=` never worked.
- "Buka Undangan" button no longer throws a JavaScript error (it referred to an
  audio element that didn't exist).
- Removed the canonical link pointing to the vendor page.
- Version 1 (online): venue replaced with Instagram live story links, Google Maps
  button removed, cover greeting set to "Sahabat-sahabat kami", RSVP & ucapan form
  removed, "no gifts" note replaced with a Wedding Gift QR section.
