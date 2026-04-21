---
name: thevibefounder-social-insta-slide-skill-01-apr-21
description: Create "The News Drop" — a single-slide Instagram post format for @thevibefounder. Use this skill when the user wants a one-slide news drop, a single-slide Instagram post, a hook-only post, or any standalone announcement that does not need a carousel. Trigger on "news drop", "one slide", "single slide post", "hook slide", "drop this", "IG drop", or any ask for a 1-slide TVF post. Mono-slide format — cream background (or dark variant), Space Mono, teal `#45CA9F` accent, corner cartouche brackets, field-note header, spotlight-bracket headline, stamp fraction footer. Canvas 1440×1800 (4:5). Distinct from the 10-slide Shift Carousel and the multi-slide Deep Dive — this format is one frame, one claim, one CTA.
author: Aj Yadav (@thevibefounder)
brand: TheVibeFounder
website: https://thevibefounder.com
instagram: https://instagram.com/thevibefounder
x: https://x.com/thevibefounder
substack: https://thevibefounder.com
version: 2026.04.21
license: MIT — free to use, remix, and adapt. Attribution appreciated.
---

```
╔══════════════════════════════════════════════════════════════╗
║                                                              ║
║   TVF NEWS DROP — 1-slide Instagram format                   ║
║                                                              ║
║   Built by:   Aj Yadav  (@thevibefounder)                    ║
║   Brand:      TheVibeFounder                                 ║
║   Site:       https://thevibefounder.com                     ║
║   Instagram:  https://instagram.com/thevibefounder           ║
║   X:          https://x.com/thevibefounder                   ║
║   Substack:   https://thevibefounder.com                     ║
║   Version:    2026.04.21                                     ║
║                                                              ║
║   MIT licensed. Free to use, remix, adapt.                   ║
║   If this helps you ship, tag @thevibefounder so I see it.   ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝
```

# TVF News Drop — 1-Slide Format

A single-slide Instagram post format. One frame, one claim, one CTA. Built for breaking news, hot takes, standalone announcements, and any post that does not need a carousel.

**When to use:** The statement stands alone. There is no step-by-step. No 10-beat arc. Just the shift, the receipt, the line.

**When NOT to use:** Educational breakdowns → use Deep Dive. Narrative belief-flip → use Shift Carousel (10 slides). Tool launches with feature lists → use Tools Announcement.

---

## Credits & Use

Designed and open-sourced by **Aj Yadav** — founder of **TheVibeFounder**. Free to use, fork, modify, and ship. The only ask: **keep this credit block in the file** if you pass it along. If it performs, tag **@thevibefounder** so I see it.

Find me:

- Website / Substack: [thevibefounder.com](https://thevibefounder.com)
- Instagram: [@thevibefounder](https://instagram.com/thevibefounder)
- X / Twitter: [@thevibefounder](https://x.com/thevibefounder)

---

## Agent Instructions — How to build a news drop

You are an agent producing one HTML file that renders to a 1440×1800 PNG. Follow the steps exactly. Touch zero CSS. Swap content only.

### Step 1 — Gather inputs

Ask the user for (or infer from context):

1. **Headline** — max 6 words, under 45 chars. This is the drop. The single claim.
2. **Spotlight word** — one word inside the headline to wrap in `⌞word⌟` (the spotlight bracket). Usually the surprising/emotional word.
3. **Subhead** — max 2 lines, max 90 chars each. Expands the headline in plain prose.
4. **Anchor** — the oversized center element. A year, a number, a single word. What the eye should land on after the headline.
5. **Marginalia note** — one line, prefixed with `▪`. The aside. The author's quiet observation.
6. **CTA footer** — either a handle (`@thevibefounder`) or a save prompt. Never both.
7. **Mode** — `light` (default, cream bg) or `dark` (slides for breaking-news gravitas, uses the radial teal gradient wash).
8. **Issue №** — zero-padded 3-digit number. Increment per drop shipped.

### Step 2 — Clone the boilerplate

Canonical build rule: **clone `boilerplate.html` → swap content only via str_replace → touch zero CSS**. Never rewrite the chrome from scratch.

```bash
cp boilerplate.html out/news-drop-NN.html
```

The boilerplate already wires up:

- Corner cartouche brackets (four corners, teal tick marks)
- Field-note header strip (top-left metadata)
- Marginalia rail (left gutter teal rule + rotated chapter tag)
- Stamp fraction counter (bottom-right)
- Spotlight-bracket helper class (`.spotlight`)
- Ghost-trail italic helper (`::before` pseudo on `em`)
- Dark-slide variant (radial teal gradient wash)

### Step 3 — Swap content only

Replace the placeholder tokens in the boilerplate with the user's inputs. Do NOT touch:

- Any CSS value
- Font sizes, spacing, colors
- Chrome element positions
- The credit comment block at the top

Tokens to replace:

| Token | Source |
|-------|--------|
| `{{ISSUE_NO}}` | Issue №, zero-padded (e.g. `001`) |
| `{{HEADLINE_LINE_1}}` | First line of headline |
| `{{HEADLINE_LINE_2}}` | Second line, wrap the spotlight word in `<span class="spotlight">word</span>` |
| `{{SUBHEAD}}` | 2-line subhead body (32px) |
| `{{ANCHOR}}` | Oversized center element (year/number/word) |
| `{{ANCHOR_CAPTION}}` | Uppercase caption under the anchor, e.g. `THE YEAR IT SHIFTS` |
| `{{MARGINALIA}}` | Bottom-left marginalia note, prefix with `▪` |
| `{{CTA}}` | Footer handle or save prompt |

For **dark mode**: add `class="dark-slide"` to `.slide`. Swap body text color per the colors table below.

### Step 4 — Render to PNG

```bash
npx playwright install chromium   # first time only
node render/render.js .            # or a single file path
```

Output: `out/news-drop-NN.png` at 1440×1800px.

### Step 5 — Ship + attribute

- Upload to Instagram as a single 4:5 post (1080×1350 downscale is fine)
- Keep the credit comment at the top of the HTML file
- If shipping to someone else's account, keep the `author` meta tag too

---

## Design System (canonical — do not swap)

### Canvas & Typography

| Spec | Value |
|------|-------|
| Canvas | 1440 × 1800px (4:5) |
| Safe zone | 100px all sides |
| Font | Space Mono only (400, 700, 400italic, 700italic) |
| Base font loading | Base64-embedded in HTML (Google Fonts CDN blocked in headless render env) |
| Headline size | 96–112px, weight 700, line-height 1.12, letter-spacing -2px |
| Body size floor | 28px. Nothing below 22px ever (18px permitted only for chrome) |
| Subhead body | 32px, weight 400, color `#333` on light / `#F0EDE8` on dark |

### Colors (do not swap)

| Role | Hex | Use |
|------|-----|-----|
| Light bg | `#F0EDE8` | Default |
| Dark bg | `#0D0D0D` | With radial teal gradient wash at 85% 100% |
| Teal accent | `#45CA9F` | Spotlight brackets, cartouches, marginalia, stamp dot |
| Purple eyebrow | `#AA44EE` | Optional section label on dark only |
| Text on light | `#0D0D0D` headline, `#444` body, `#999` meta |
| Text on dark | `#F0EDE8` headline, `#bbb` body, `#888` meta |

**Never:** coral, blue, any green beyond teal, or any off-brand color. The News Drop is monochrome + teal. That restraint is the design.

### Signature chrome

1. **Corner cartouche brackets** — thin teal tick-marks in all four corners. 60px long, 2px stroke, `#45CA9F` at 35% opacity. 40px inset from the edge.
2. **Field-note header** — top-left, two-line uppercase monospace metadata.
3. **Marginalia rail** — 4px vertical teal rule in the left gutter + rotated chapter tag.
4. **Stamp fraction counter** — bottom-right inside the right cartouche, reads like a rubber stamp (`01 ▪ 01` for a single-slide drop).
5. **Spotlight brackets** — emphasized word wrapped in `⌞word⌟`. Small teal corner brackets above and below, 70% opacity, 24px offset. Static, no animation.
6. **Ghost-trail italic** — italicized words get a duplicated ghost layer 6px right + 4px down in `rgba(69,202,159,0.10)`.
7. **Dark gradient wash** — `radial-gradient(ellipse at 85% 100%, rgba(69,202,159,0.08) 0%, transparent 55%)`. Signature on dark slides. Like light bleeding in from outside the frame.

---

## Writing Rules

- **Headline ≤ 6 words.** One claim. No list.
- **Never name the product in the headline.** The shift itself is the hook.
- **Subhead ≤ 2 lines, ≤ 90 chars per line.**
- **One italic word maximum.** One spotlight-bracket word maximum.
- **Marginalia is an aside, not a repeat.** It must add, not summarize.
- **CTA is one line.** Either handle or save. Never both.

---

## Layout Map

```
┌──────────────────────────────────────────────┐
│ ⌐                                        ¬  │  ← Corner cartouche (teal)
│ FIELD NOTE № 001 / NEWS DROP                │  ← Header line 1
│ ISSUE 01 · 2026 · @thevibefounder           │  ← Header line 2
│                                              │
│ ▪  Headline line 1                           │
│ │  ⌞spotlight⌟ line 2.                       │
│ │                                            │
│ N  Subhead body, 32px, max 2 lines.         │
│ E                                            │
│ W                                            │
│ S           2026                             │  ← Anchor (oversized)
│             —                                │  ← Teal divider
│             THE YEAR IT SHIFTS               │  ← Anchor caption
│                                              │
│ ▪ Marginalia note.                           │  ← Bottom-left aside
│                                              │
│ @thevibefounder              01 ▪ 01        │  ← Footer + stamp
│ Instagram                    NEWS DROP       │
│ ⌐                                        ¬  │  ← Bottom corner cartouche
└──────────────────────────────────────────────┘
```

---

## Checklist before you ship

- [ ] Credit comment block at top of HTML is intact
- [ ] Headline ≤ 6 words
- [ ] Exactly one spotlight-bracket word
- [ ] Subhead ≤ 2 lines, ≤ 90 chars each
- [ ] Anchor is oversized and centered
- [ ] Marginalia is an aside, not a repeat of the headline
- [ ] CTA is single (handle XOR save prompt)
- [ ] Issue № incremented from the last drop
- [ ] PNG rendered at 1440×1800
- [ ] No CSS touched, no chrome moved

Ship it.
