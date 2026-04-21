# thevibefounder.com

Public source for **[thevibefounder.com](https://thevibefounder.com)** — the TVF home and skills directory. Deployed via Cloudflare Pages.

## Structure

```
/index.html                       — apex landing
/skills/index.html                — skills hub
/skills/<slug>/index.html         — skill detail page
/skills/<slug>/<bundle>.zip       — downloadable skill bundle
/skills/<slug>/SKILL.md …         — loose source files (browsable on GitHub)
```

Each skill gets a short memorable URL (`/skills/news-drop/`). Inside the folder, the zip and SKILL.md keep the self-documenting full skill ID (`thevibefounder-social-insta-slide-skill-01-apr-21`) so the agent-facing name stays explicit.

## How people get a skill

1. Visit `/skills/` and pick a skill
2. Click **Download skill** on the detail page → direct GitHub download
3. Unzip into `.claude/skills/<id>/` and they're set

No email gate, no account. Open source bundle, MIT licensed.

## Skills shipped

| # | Slug | Name | Status |
|---|------|------|--------|
| 01 | [`news-drop`](./skills/news-drop/) | TVF News Drop — 1-Slide Instagram Post | Live |

## License

MIT — see [LICENSE](./LICENSE). Skill bundles ship with their own license.

## Links

- [thevibefounder.com](https://thevibefounder.com) · [letter.thevibefounder.com](https://letter.thevibefounder.com) · [@thevibefounder](https://instagram.com/thevibefounder)
