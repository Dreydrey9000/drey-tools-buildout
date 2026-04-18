# drey tools buildout

Meta / task tracker for the 11 UI-challenge apps being shipped as dreytools.com subdomains.

Each app has its **own git repo** — this is not a monorepo.

## Shipped (4/11)

| URL | Repo | Folder |
|---|---|---|
| [player.dreytools.com](https://player.dreytools.com) | [dreytools-player](https://github.com/Dreydrey9000/dreytools-player) | `~/My Apps/dreytools-player/` |
| [showcase.dreytools.com](https://showcase.dreytools.com) | [dreytools-showcase](https://github.com/Dreydrey9000/dreytools-showcase) | `~/My Apps/dreytools-showcase/` |
| [contact.dreytools.com](https://contact.dreytools.com) | [dreytools-contact](https://github.com/Dreydrey9000/dreytools-contact) | `~/My Apps/dreytools-contact/` |
| [templates.dreytools.com](https://templates.dreytools.com) | [dreytools-templates](https://github.com/Dreydrey9000/dreytools-templates) | `~/My Apps/dreytools-templates/` |

## Pending

See [TASKS.md](./TASKS.md) for the full roadmap and ship order. Quick list:

1. Product page for dreythomas.com (unlocks Stripe)
2. Weather widget for Life Dashboard
3. Chat UI (Dottie web OR ABS Club)
4. Calendar / Scheduling at scheduling.dreytools.com
5. Dashboard UI (pick a vertical first)
6. Task Management board (1BB Community Platform feature)
7. Life Dashboard guest mode (remove showcase sign-in friction)
8. Website Council audit of templates (then revise)

## Visual

Open [diagram.html](./diagram.html) in a browser for the integration map.

## Convention

Each subproject:
- Own git repo under Dreydrey9000
- Own Cloudflare Pages project (`dreytools-<name>`)
- Own custom subdomain on dreytools.com
- Single-file HTML + CSS + vanilla JS, zero build step
- Warm dark + bold + cyan brand
