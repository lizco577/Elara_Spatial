# Elara Spatial — Website Design Iterations

Static HTML prototypes exploring directions for the Elara Spatial marketing site.
Every iteration is a single self-contained `.html` file — no build step, no
dependencies. Open `index.html` and click through from there.

## Viewing

Open `index.html` in a browser. It's an index of every iteration, with a live
hover preview of each one and a pin control for bookmarking favourites.

Iterations are designed for **desktop at 1440px** and are not responsive.

## Iterations

| | Direction | Pages | Notes |
|---|---|---|---|
| **00** | Wireframes | All 7 | Greyscale structure. Working FAQ accordions and contact form. |
| **01** | Desktop Foundation | 4 | First visual pass. Loader intro that morphs into the nav logo. |
| **02** | Bento Style | 4 | Floating glass pill nav, full-bleed hero card, dark bento overview grid. |
| **03** | Full Bleed | 4 | Edge-to-edge hero video, full-width nav bar, light-mode bento, gradient stat cards. |
| **04** | Moodboard Based | 3 | Brand tokens with contour fields, glyph lattice and gradient orbs. |
| **05** | Editorial | 3 | Restrained, whitespace-driven. Paper-white canvas, light display type, hairline rules. |
| **06** | **Editorial (Complete)** | All 7 | Current direction. Extends 05 with the remaining pages, bento overview, hero video and loader intro. |
| **07** | Luma Site | 1 | Microsite for the LUMASITE product. Same editorial system, lavendar-led instead of magenta. Scroll-scrubbed video section, counter-scrolling columns, scroll-driven marquee. |
| **08** | Luma Site (Mark-led) | 1 | Closer to the Figma. Real LUMASITE lockup, Figma nav. Pinned old-way/new-way maze, pinned platform story, scroll-driven marquee, loader intro. |
| **09** | Luma Site (Alt hero) | 1 | Identical to 08. The only difference is the hero video (interiorscroll.mp4, autoplaying on a loop). |
| **10** | Editorial (Working copy) | All 7 | A copy of 06, taken as a working surface so the 06 direction stays intact. |

**Iteration 06 is the live working direction.** Earlier iterations are kept as a
record of the exploration.

## Brand

Tokens follow the Elara Spatial brand guidelines:

- **Type** — Geist for headlines, Inter for body
- **Colour** — magenta `#FF00FF`, cyan `#00FFFF`, lavendar `#7F80FF`, black, white
- **On light backgrounds** the accessible dark variants are used instead:
  `#D000D0`, `#008282`, `#6566D9`
- **Pattern** — contour lines and a lattice built from the three glyph blocks
  (outer shell, diamond, dot)
- **Gradient** — linear across surfaces, angular reserved for the logomark

## Assets

`/assets` holds the files this project depends on:

| File | Used by |
|---|---|
| `homepage_hero_new.mp4` | Hero video, iterations 03 and 06 |
| `scrollworld.mp4` | Scroll-scrubbed Responsible AI section (06); hero loop (07) |
| `interiorscroll.mp4` | Scroll-scrubbed Deployment section (06); Platform section (07) |
| `Subtract*.png` | Adoption scroll story, iteration 06 |
| `Group 2147204186*.png` | Leadership portraits, iteration 06 |
| `Contour lines.svg` | Contour pattern, inlined as a CSS mask in iteration 06 |
| `Contour lines pink.png` | Reference render of the contour pattern |
| `No app - phone in hand.png` | Bento "phone camera only" card, iteration 06 |

### Known issue: expiring image links

Images exported through the Figma MCP are served from a CDN that **expires them
after roughly 7 days**. Several iterations still reference those URLs and will
show empty image boxes:

- **iterations 01, 02, 03** — ~50 references, already past their window.
  Treated as archive; layout and copy still read correctly.
- **iteration 06** — 3 references remaining in the bento overview.

The durable fix is to export the image from Figma, drop it into `/assets`, and
point the `src` at a relative path — as already done for the hero video, the
contour SVG and the phone-in-hand plate.

## Structure

```
index.html            iteration index with hover previews and pinning
iteration-00.html     wireframes
iteration-01.html  …  iteration-06.html
assets/               video, patterns, image plates
```
# Elara_Spatial
# Elara_Spatial
