# drey tools buildout

Meta / task tracker for the 11 UI-challenge apps shipped as dreytools.com subdomains.

Each app has its **own git repo** — this is not a monorepo.

## All 11 Shipped

| URL | Repo | Folder |
|---|---|---|
| [player.dreytools.com](https://player.dreytools.com) | [dreytools-player](https://github.com/Dreydrey9000/dreytools-player) | `~/My Apps/dreytools-player/` |
| [showcase.dreytools.com](https://showcase.dreytools.com) | [dreytools-showcase](https://github.com/Dreydrey9000/dreytools-showcase) | `~/My Apps/dreytools-showcase/` |
| [contact.dreytools.com](https://contact.dreytools.com) | [dreytools-contact](https://github.com/Dreydrey9000/dreytools-contact) | `~/My Apps/dreytools-contact/` |
| [templates.dreytools.com](https://templates.dreytools.com) | [dreytools-templates](https://github.com/Dreydrey9000/dreytools-templates) | `~/My Apps/dreytools-templates/` |
| [weather.dreytools.com](https://weather.dreytools.com) | [dreytools-weather](https://github.com/Dreydrey9000/dreytools-weather) | `~/My Apps/dreytools-weather/` |
| [chat.dreytools.com](https://chat.dreytools.com) | [dreytools-chat](https://github.com/Dreydrey9000/dreytools-chat) | `~/My Apps/dreytools-chat/` |
| [dashboard.dreytools.com/demo](https://dashboard.dreytools.com/demo) | [life-dashboard](https://github.com/Dreydrey9000/life-dashboard) | `~/My Apps/life-dashboard/` |
| [product.dreytools.com](https://product.dreytools.com) | [dreytools-product](https://github.com/Dreydrey9000/dreytools-product) | `~/My Apps/dreytools-product/` |
| [scheduling.dreytools.com](https://scheduling.dreytools.com) | [dreytools-scheduling](https://github.com/Dreydrey9000/dreytools-scheduling) | `~/My Apps/dreytools-scheduling/` |
| [tasks.dreytools.com](https://tasks.dreytools.com) | [dreytools-tasks](https://github.com/Dreydrey9000/dreytools-tasks) | `~/My Apps/dreytools-tasks/` |
| [admin.dreytools.com](https://admin.dreytools.com) | [dreytools-admin](https://github.com/Dreydrey9000/dreytools-admin) | `~/My Apps/dreytools-admin/` |

## Convention

Each subproject:
- Own git repo under `Dreydrey9000`
- Own Cloudflare Pages project named `dreytools-<name>`
- Own custom subdomain on dreytools.com
- Single-file `index.html` + CSS + vanilla JS, zero build step
- Warm dark (#0a0908) + cyan accent (#22d3ee)
- Mobile-first, safe-area insets, iOS zoom-blocker

## Deploy pattern

```bash
cd ~/My\ Apps/dreytools-<name>
wrangler pages deploy . --project-name dreytools-<name> --branch main
```

Custom domain + DNS wiring recipe: see `~/.claude/projects/-Users-andrethomas/memory/reference_cloudflare_dns_token.md`

## Planning docs

- [TASKS.md](./TASKS.md) — original 11-app roadmap + ship waves
- [diagram.html](./diagram.html) — visual integration map
- `~/Desktop/MORNING-REPORT.md` — overnight council audit (Website Builder + Brand) with ranked revision list
