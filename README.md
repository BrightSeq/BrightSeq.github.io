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

- Chalkdoku's game privacy policy, at `en/games/chalkdoku/privacy/`. Today it is a placeholder shell: `noindex`, not in `sitemap.xml`, not linked from other pages, sections 2-11 say "To be completed before release". Do not give its URL to Play Console, and do not link it or add it to the sitemap, until the real text is in (generate it from the game repo's `docs/legal/privacy-policy.md` once the shipped build matches every statement). The draft describes planned AdMob, Firebase Analytics, Crashlytics and Play Billing; those SDKs are not in the game yet. When the real text goes in, drop `noindex`, link it from the game page's Privacy section, and add it to the sitemap.
- Organization phone number. Play Console asks for one on an organization account, and it is shown on Google Play. It is not on this site because none has been provided.
- Chalkdoku's store link. Add it only after the Play listing is public.
- `app-ads.txt` at the site root. Add it only if a released build shows ads.

The website privacy notice at `en/privacy/` covers this static site only. It is not the game policy.

Play Console associates the site by a Search Console ownership link, not by the text alone. Register `https://brightseq.com/` in Search Console with the same Google account that owns the Play Console developer account, then send the website verification request from Play Console → Account details. The payments profile legal name and address must match the Dun & Bradstreet record. See [Verify your website](https://support.google.com/googleplay/android-developer/answer/13205715).

## Brand

The mark is a striped sun cut by a single diagonal line: the stripes are the sequence (序), the sun is the light (明). Official source files are in [source/brand/sun-slash/](source/brand/sun-slash/): colour icon (rounded, square, bare sun on transparent), one-colour black and white, a simplified small-size icon for 16/24/32 px (4 stripes, larger sun), PNGs from 16 to 1024 px, `favicon.ico`, and horizontal and vertical lockups (each also on dark). `source/brand/sun-slash/png/` holds the exports.

Website files in `assets/brand/` keep their original names and URLs; only the artwork changed:
- `icon-16/32/64/192/512.png`, `apple-touch-icon.png`, root `favicon.ico`: the sun icon (16/32 use the small-size variant).
- `logo-512.png`, `logo-master.png`: the same icon at larger sizes (`logo-512.png` is the `logo` in the Organization JSON-LD).
- `lockup-vertical.png` (icon above the name) is the home page hero image; `lockup-horizontal.png` is the same set side by side.
- `social-preview.png` (1200x630, linked from `en/index.html` via og:image): vertical lockup plus the line "Small games. Careful puzzles.".
- Wordmark (`wordmark.svg` for light backgrounds, `wordmark-on-dark.svg`, `wordmark-mono-dark.svg` / `wordmark-mono-light.svg` for one colour) is unchanged: Fraunces Bold converted to outlines with a deep-green-to-lantern-amber gradient and a lit dot in the last `q`; sources in `source/brand/wordmark/`.
- Play listing icon source: `source/brand/play-icon-512.png` (full-bleed square, no rounded corners) and `source/brand/icon-1024.png`.

Other brand folders in `source/brand/`:
- [sun-mark/](source/brand/sun-mark/): the earlier stair-cut version of the sun (each stripe ends one step further left). Kept as an alternative; not used on the site.
- The original clay cave-and-lantern artwork (`logo-original.jpg`, `icon-cave-source.jpg`, `simple.svg`, `simple-line.svg`) is kept for reference.

Keep the URLs in `assets/brand/` stable when updating artwork. Colours: tile `#0A2D21` to `#17553E`, sun `#FFF3CC` through `#FFC857` to `#EE7B1A`, page background `#f4f2ea`.
