# My Music — twenty songs, five singers

Course: **Introduction to Digital Services — DIG001IT1AE-3033 (Chengdu)**
Topic chosen by me: **a personal music collection** — five singers, twenty tracks, in the order I
actually listen to them.

> Three pages, HTML + CSS only, **no JavaScript**, 0 errors in the W3C validator, about 55 kB in total.

---

## Pages

| File | Content |
|---|---|
| `index.html` | Home — the idea behind the collection, three doors into the site, and a genre table counted from the playlist |
| `singers.html` | Five profiles: Gareth.T, Top Barry, Stefanie Sun, keshi, Lu Guangzhong, plus the six guest names that appear once each |
| `songs.html` | The playlist: all twenty tracks in order with genre and a note, a waveform, and a “recommend a song” form |

Assets: `css/style.css` (one stylesheet, 11 numbered sections), `images/` (seven SVG drawings:
five singer sleeves, a vinyl record, a waveform).

## The twenty tracks

| # | Track | Artist | Genre |
|---|---|---|---|
| 1 | Winter Comes Again | Luo Yan | Chinese pop |
| 2 | Waves | Gareth.T | R&B |
| 3 | 2 More Weeks | Gareth.T | Indie pop |
| 4 | DD Backseat | Top Barry · Rapeter | Hip-hop |
| 5 | Rise to Fame | Top Barry · INDEcompany | Rap |
| 6 | Hidden Album (Remix) | Top Barry · INDEcompany | Rap |
| 7 | Name Engraved in My Heart | Lu Guangzhong | Indie rock |
| 8 | Marry | Top Barry · INDEcompany | Rap |
| 9 | Sing Love Songs with My Back | Gareth.T | R&B |
| 10 | Emergency Contact | Gareth.T | R&B |
| 11 | Finally Understand | Stefanie Sun | Mandopop |
| 12 | I Am Not Sad | Stefanie Sun | Mandopop |
| 13 | Rainy Day | Stefanie Sun | Mandopop |
| 14 | You Look Lonely | Cassanova | Alt pop |
| 15 | Want You | Clara La San | Alt R&B |
| 16 | Face Like Jade | Li Daben BENZO | Chinese pop |
| 17 | WANTCHU | keshi | Lo-fi |
| 18 | Forget You in the Arctic | Gareth.T | Indie pop |
| 19 | Rent Purchase | Joker Xue | Chinese pop |
| 20 | I'm Here for You | Guo Yifan | Chinese pop |

## What changed from my first draft

My first version used black text on a dark red background, which is unreadable: the contrast ratio was
about 2:1. The palette here is measured instead:

| Role | Hex on `#14090C` | Contrast | Used for |
|---|---|---|---|
| Body text | `#F7E9E4` | ≈ 15.6:1 | paragraphs, table cells |
| Muted text | `#C1A9A4` | ≈ 8.6:1 | notes, captions |
| Amber | `#F0B357` | ≈ 9.9:1 | links, genre tags |
| Coral | `#E0574A` | ≈ 5.2:1 | current page, hot badges, primary button |

All four pass WCAG AA for normal text. Headings are set in **DM Serif Display**, body and labels in
**Inter**, both from Google Fonts with local fallbacks.

## How the course requirements are met

| Requirement | Where |
|---|---|
| Scope: 3 pages | home, singers, songs — one navigation bar, current page marked |
| Semantic HTML5 | `header`, `nav`, `main`, `section`, `article`, `table`, `footer` |
| Table | genre table on the home page, playlist table on the songs page, guest table on the singers page — all with `caption` and `th scope` |
| List | track lists inside each singer profile, the four listening rules |
| Buttons | two real `<button>` elements in the recommendation form (submit and reset) |
| Images on every page | 1 + 5 + 1 drawings, each with descriptive `alt` |
| Navigation | three pages, same bar, `aria-current` on the active link |
| Optimised media | seven SVG files, 10 kB in total; no bitmaps, no web fonts downloaded as images |
| Responsive | breakpoints at 900 px and 680 px; tables scroll inside their own box |
| Accessible | skip link, 2 px focus ring, `alt`, `lang`, `prefers-reduced-motion`, contrast checked |
| Style in a separate stylesheet | `css/style.css`, linked from every page, no `<style>` blocks |
| Valid HTML5 | 0 errors, 0 warnings in the W3C Nu validator on all three pages |
| No JavaScript | 0 lines |

## Why the singer artwork is drawn, not photographed

The five sleeves are SVG drawings of a record sleeve with a monogram, not photographs of the artists.
Real portraits of these singers are copyrighted, and using a photo of a person to represent them would
also be a likeness question — a record sleeve with initials is honest, legal, and keeps the page weight
at 1 kB per image.

## Run it locally

```bash
python -m http.server 8000
# then open http://127.0.0.1:8000
```

## Publish on GitHub Pages

1. Create a new **public** repository, for example `my-music`.
2. Choose **uploading an existing file** and drag in `index.html`, `singers.html`, `songs.html`,
   `README.md`, `css/` and `images/`.
3. Commit.
4. **Settings → Pages → Source: Deploy from a branch → main, folder `/ (root)` → Save.**
5. After a minute: `https://<username>.github.io/my-music/`.

## The two links for Moodle

```
repository: https://github.com/<username>/my-music
page:       https://<username>.github.io/my-music/
```

## Before submitting

`singers.html` and `songs.html` contain `you@example.com` as the mail address of the recommendation
form; replace it with a real address (two places in `songs.html`, none elsewhere).
