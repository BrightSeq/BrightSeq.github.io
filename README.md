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

Contact email, wordmark (the logo medallion is in `assets/brand/`; small sizes use `icon-*.png`, the zoomed-in lantern version), Chalkdoku's privacy policy text (depends on which SDKs the game ships with), support page, Chalkdoku store link (add only after the Play listing is public).
