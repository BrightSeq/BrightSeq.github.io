# EmbedGrad website

Static HTML/CSS for GitHub Pages (organisation site, repo `EmbedGrad/embedgrad.github.io`, public). No build step, no external fonts, no analytics, no JavaScript. English only. The root redirects to `/en/`, same layout as the MonsoonIsle site so game pages live under `/en/games/<game-slug>/`.

- Home: https://embedgrad.github.io/en/
- Preview locally: `python3 -m http.server 8080` in this directory, then open http://localhost:8080/
- Publish: commit and push to the branch set in Settings → Pages (`main`, root).

## Add a game

1. Add a card to `en/index.html` (link only to pages that exist).
2. Put the privacy policy at `en/games/<game-slug>/privacy/index.html`, with `<link rel="canonical">` set to its own URL, and use that URL in Play Console and in the game.
3. Add the page to `sitemap.xml`.
4. Support page and `app-ads.txt` (root, only if the game shows ads) are added when decided.

## Not decided yet

Contact email (the logo medallion is in `assets/brand/`; `logo-*.png` is the detailed illustrated medallion for big placements; the simple app icon is a clay-style cave mouth with a lantern and stone steps, generated from the medallion (`icon-*.png`, `apple-touch-icon.png`, `favicon.ico`; source `~/Tools/embedgrad-brand/icon-cave-source.jpg`, Play 512 px in `play-icon-512.png`), Chalkdoku's privacy policy text (depends on which SDKs the game ships with), support page, Chalkdoku store link (add only after the Play listing is public).


Brand files in `assets/brand/`: wordmark (`wordmark.svg` for light backgrounds, `wordmark-on-dark.svg`, `wordmark-mono-dark.svg` / `wordmark-mono-light.svg` for one-colour use), `lockup-horizontal.png`, `lockup-vertical.png`, `social-preview.png` (1200x630, linked from `en/index.html` via og:image). The wordmark is Fraunces Bold converted to outlines with a deep-green-to-lantern-amber gradient and a lit dot in the last `d`; sources in `~/Tools/embedgrad-brand/wordmark/`.
