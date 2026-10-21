# BrightSeq website

Static HTML/CSS for GitHub Pages (organisation site, repo `BrightSeq/BrightSeq.github.io`, public). No build step, no external fonts, no analytics, no executable JavaScript. English only. The root redirects to `/en/`, same layout as the MonsoonIsle site so game pages live under `/en/games/<game-slug>/`.

- Home: https://brightseq.com/en/
- Chalkdoku: https://brightseq.com/en/games/chalkdoku/
- Chalkdoku support: https://brightseq.com/en/games/chalkdoku/support/
- Website privacy: https://brightseq.com/en/privacy/
- Preview locally: `python3 -m http.server 8080` in this directory, then open http://localhost:8080/
- Publish: commit and push to the branch set in Settings → Pages (`main`, root). Ask before pushing.

## Add a game

1. Add a card to `en/index.html` (link only to pages that exist).
2. Put the privacy policy at `en/games/<game-slug>/privacy/index.html`, with `<link rel="canonical">` set to its own URL, and use that URL in Play Console and in the game.
3. Add the page to `sitemap.xml`.
4. Support page and `app-ads.txt` (root, only if the game shows ads) are added when decided.

## Identity on the site

- Studio name: BrightSeq.
- Legal entity: 安徽明序科技有限公司 (Anhui Mingxu Technology Co., Ltd). The Chinese name is the registered name.
- Registered address: 安徽省淮南市田家庵区朝阳街道龙湖路金大地龙湖中心3栋1003, 232000, China. This is the address on the verified Google payments profile.
- Company email: mingxufortune@gmail.com. This is the address in the footer, the contact section and the website privacy notice.
- Chalkdoku support stays mengjingchanyu@gmail.com. Do not replace it with the company email.
- The home page includes one `application/ld+json` Organization block. It is data for crawlers, not page behaviour. There is still no executable JavaScript.

## Still open

- Chalkdoku's game privacy policy, at `en/games/chalkdoku/privacy/`. Do not publish it until the game is ready for review. The draft describes planned AdMob, Firebase Analytics, Crashlytics and Play Billing; those SDKs are not in the game yet.
- Organization phone number. Play Console asks for one on an organization account, and it is shown on Google Play. It is not on this site because none has been provided.
- Chalkdoku's store link. Add it only after the Play listing is public.
- `app-ads.txt` at the site root. Add it only if a released build shows ads.

The website privacy notice at `en/privacy/` covers this static site only. It is not the game policy.

Play Console associates the site by a Search Console ownership link, not by the text alone. Register `https://brightseq.com/` in Search Console with the same Google account that owns the Play Console developer account, then send the website verification request from Play Console → Account details. The payments profile legal name and address must match the Dun & Bradstreet record. See [Verify your website](https://support.google.com/googleplay/android-developer/answer/13205715).

## Brand

The logo medallion is in `assets/brand/`. `logo-*.png` is the detailed illustrated medallion for large placements. The simple app icon is a clay-style cave mouth with a lantern and stone steps, generated from the medallion (`icon-*.png`, `apple-touch-icon.png`, `favicon.ico`; source `source/brand/icon-cave-source.jpg`, Play 512 px in `source/brand/play-icon-512.png`).

Brand files in `assets/brand/`: wordmark (`wordmark.svg` for light backgrounds, `wordmark-on-dark.svg`, `wordmark-mono-dark.svg` / `wordmark-mono-light.svg` for one-colour use), `lockup-horizontal.png`, `lockup-vertical.png`, `social-preview.png` (1200x630, linked from `en/index.html` via og:image). The wordmark is Fraunces Bold converted to outlines with a deep-green-to-lantern-amber gradient and a lit dot in the last `q`; sources in `source/brand/wordmark/`.

The complete brand working set is kept in [source/brand/](source/brand/), including the original logo, icon artwork, simplified SVGs, store-size exports and wordmark variants. Use `assets/brand/` for website-facing exports and keep their URLs stable when updating artwork.
