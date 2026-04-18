# Drey Tools Buildout

Monorepo of 11 UI challenge mini-apps → real dreytools.com properties.

## Live subdomains

| Sub | What | Folder |
|---|---|---|
| [player.dreytools.com](https://player.dreytools.com) | DR. DREY music player | `music-player/` |
| [showcase.dreytools.com](https://showcase.dreytools.com) | Three-card tools showcase | `profile-card/` |
| [contact.dreytools.com](https://contact.dreytools.com) | Chat-app-style contact | `contact-form/` |
| [templates.dreytools.com](https://templates.dreytools.com) | Landing page template library | `templates/` |

## Stack

Pure HTML + CSS + vanilla JS per app. Cloudflare Pages for hosting. Custom domains auto-wired via CF API.

## Deploy a subproject

```bash
cd <subproject>
wrangler pages deploy . --project-name dreytools-<name> --branch main
```

## See

- [TASKS.md](./TASKS.md) — full 11-app roadmap and ship waves
- [diagram.html](./diagram.html) — visual integration map
- Each subfolder has its own README with component-level details
