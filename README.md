# thevibefounder.com

Public source for **[thevibefounder.com](https://thevibefounder.com)** — the TVF home and skills directory. Deployed via Cloudflare Pages.

## Structure

```
/index.html                                                      — apex landing
/skills/index.html                                               — skills hub
/skills/thevibefounder-social-insta-slide-skill-01-apr-21.html   — skill 01
```

Skills follow the naming convention `thevibefounder-<category>-<slug>-skill-<NN>-<date>` so the repo stays self-documenting as more skills ship.

## How people get a skill

1. Visit `/skills/` and pick a skill
2. Drop their email on the detail page
3. Get a signed, time-limited download link emailed + auto-triggered

Bundles are hosted on R2 and distributed via a Cloudflare Worker. Infrastructure lives outside this repo; this repo is only the public site.

## Skills shipped

| # | Skill | Format | Status |
|---|-------|--------|--------|
| 01 | [thevibefounder-social-insta-slide-skill-01-apr-21](./skills/thevibefounder-social-insta-slide-skill-01-apr-21.html) | 1-slide Instagram post · Claude Code skill | Live |

## License

MIT — see [LICENSE](./LICENSE). Skill bundles ship with their own license.

## Links

- [thevibefounder.com](https://thevibefounder.com) · [letter.thevibefounder.com](https://letter.thevibefounder.com) · [@thevibefounder](https://instagram.com/thevibefounder)
