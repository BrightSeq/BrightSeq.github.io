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

- Chalkdoku's game privacy policy, at `en/games/chalkdoku/privacy/`. Since 2026-10-23 it holds the game repo's provisional text (effective 6 November 2026, written for planned SDKs that are not in the game yet). It is generated: `python3 <game repo>/tools/release/policy_html.py en/games/chalkdoku/privacy/index.html` (`--check` to compare); never edit the policy text here by hand. It stays `noindex`, not linked from other pages and not in `sitemap.xml` until the shipped build matches every statement; then drop `noindex`, link it from the game page's Privacy section and add it to the sitemap. The URL may be given to AdMob and Play Console now; the open items are tracked in the game repo's `docs/todo.md` (隐私政策发布前待补).
