# TVF News Drop — 1-Slide Format

> A single-slide Instagram post format for breaking news, hot takes, and standalone announcements. Free, MIT-licensed, open-sourced by @thevibefounder.

**Canvas:** 1440 × 1800px (4:5) · **Font:** Space Mono · **Accent:** Teal `#45CA9F`

---

## What's in the box

| File | Purpose |
|------|---------|
| `SKILL.md` | Full agent instructions — design system, layout, rules, checklist |
| `boilerplate.html` | Drop-in HTML template with all chrome wired up |
| `README.md` | This file |

## 60-second start

```bash
# 1. Install deps (once)
npm install
npx playwright install chromium

# 2. Clone the boilerplate
cp boilerplate.html my-news-drop.html

# 3. Edit the {{placeholders}} with your copy

# 4. Render
node render/render.js my-news-drop.html
```

Output: a 1440×1800 PNG at `out/my-news-drop.png`.

## When to use

- Breaking news
- Hot takes
- Standalone announcements
- Any post where the statement stands alone (no carousel)

## When NOT to use

- Educational step-by-step → use **Deep Dive**
- Narrative belief-flip → use **Shift Carousel** (10 slides)
- Tool feature launches → use **Tools Announcement**

## Credits

Built by **Aj Yadav** — founder of **TheVibeFounder**.

- Website / Substack: [thevibefounder.com](https://thevibefounder.com)
- Instagram: [@thevibefounder](https://instagram.com/thevibefounder)
- X: [@thevibefounder](https://x.com/thevibefounder)

Free to use, remix, and adapt. If this helps you ship, tag **@thevibefounder** so I can see it.

## License

MIT — see [LICENSE](./LICENSE).
