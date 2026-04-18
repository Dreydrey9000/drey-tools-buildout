# Drey Tools Buildout — 11 UI Challenges

**Created:** 2026-04-17
**Source:** UI project challenge list (hardest → easiest)
**Goal:** Ship all 11 as dreytools properties OR absorb into existing live apps.
**Strategy:** Dave's consolidation audit first. Don't duplicate what's already shipping.

---

## Dave's Verdict at a Glance

| # | Project | Complexity | Status | Action | Home |
|---|---------|-----------|--------|--------|------|
| 1 | Dashboard UI | 6/12 (Hardest) | ABSORB | Build as G3AC ops dashboard or ABS Club metrics | existing Life Dashboard stack |
| 2 | Task Management Dashboard | 9/12 | ABSORB | Become 1BB Community task board feature | 1BB Community Platform |
| 3 | Calendar / Event App | 8/12 | NEW | Strategic — scheduling.dreytools.com | new subdomain |
| 4 | E-commerce Product Page | 4/12 | ABSORB | Ship Stripe product pages | dreythomas.com |
| 5 | Product Landing Page | 5/12 | NEW | Template factory | templates.dreytools.com |
| 6 | Chat UI (WhatsApp Clone) | 10/12 | ABSORB | Web chat for Dottie + ABS Club chat | Dottie / ABS Club |
| 7 | Weather App | 11/12 | ABSORB | Widget on Life Dashboard | dashboard.dreytools.com |
| 8 | Music Player App | 7/12 | ABSORB | DREY AI Musician needs this NOW | drdrey.com |
| 9 | Contact Us Form | 3/12 | ABSORB | Template used across all sites | shared component |
| 10 | Profile Card UI | 2/12 | ABSORB | Team/People Hub public directory | dreythomas.com / 1BB |
| 11 | Practice Frontend | 1/12 | SKIP | Intro slide only | — |

**Net:** 8 absorb into existing apps, 2 new standalone dreytools properties, 1 skip.
**Shipping order:** Easy-absorb wins first (build templates once, reuse), then standalone NEW apps, then Dashboard-class heavy builds.

---

## Build Order (Ship > Perfect)

### Wave 1 — Reusable Components (ship this week)
These become templates used across every existing app. One build, many wins.

- [ ] **#10 Profile Card UI** — Build as reusable component. Use on dreythomas.com team page + public People Hub directory page.
  - Effort: 2 hrs
  - Lives in: shared `/components/ProfileCard` in dreythomas.com repo

- [ ] **#9 Contact Us Form** — Build once with Zod validation + Resend email. Drop into dreythomas.com, 1BB, Built By Drey.
  - Effort: 3 hrs
  - Lives in: shared `/components/ContactForm` + `/api/contact` route

- [ ] **#4 E-commerce Product Page** — Unlocks Stripe on dreythomas.com (currently pending per memory).
  - Effort: 1 day
  - Lives in: dreythomas.com `/products/[slug]`

### Wave 2 — App Features (ship next week)
These fill active gaps in live apps.

- [ ] **#8 Music Player App** — DREY AI Musician (drdrey.com) needs a player UI. Perfect fit.
  - Effort: 1 day
  - Lives in: drdrey.com `/player`
  - Unlocks: Suno-generated tracks get a playable surface

- [ ] **#7 Weather App** — Widget on Life Dashboard. Uses OpenWeather API.
  - Effort: 4 hrs
  - Lives in: dashboard.dreytools.com `<WeatherCard />`

- [ ] **#6 Chat UI** — Two homes:
  - (a) Dottie web-chat interface at dottie.dreytools.com (complements the phone channel)
  - (b) ABS Club community chat (Skool killer feature)
  - Effort: 2 days for Dottie web, 3 days for ABS Club chat with realtime
  - Decision needed: Dottie first or ABS Club first? Drey picks.

### Wave 3 — New Standalone Properties
These are NEW dreytools subdomains with strategic value.

- [ ] **#5 Product Landing Page → templates.dreytools.com** — Template library Drey can fork for every new launch.
  - Effort: 2 days for v1 (3 templates: SaaS, Info Product, Physical Product)
  - Strategic value: Every future Drey launch uses this as starting point

- [ ] **#3 Calendar / Event App → scheduling.dreytools.com** — Full calendar + event management.
  - Effort: 4 days
  - Strategic value: Could replace Cal.com for Drey. Wires into Dottie for phone-booking.

### Wave 4 — Heavy Build
Save for last. Needs clear purpose before building.

- [ ] **#1 Dashboard UI** — DO NOT build generic. Pick a vertical:
  - Option A: G3AC ops dashboard (if allowed per PPA confidentiality — probably not public)
  - Option B: ABS Club metrics dashboard (member count, shipped projects, streaks)
  - Option C: Viral Editz internal client dashboard
  - Effort: 1 week
  - Decision needed: Which vertical? Drey picks.

- [ ] **#2 Task Management Dashboard** — Feature inside 1BB Community Platform (currently in backlog).
  - Effort: 1 week
  - Unblocks: 1BB Community Platform backlog item
  - Decision needed: Build standalone first for practice, or wait for 1BB Community Platform to start?

### Skip
- ~~#11 Practice Frontend~~ — Title slide only. Not a real build.

---

## Integration Map — What Connects to What

```
dreythomas.com (existing)
  + ProfileCard component  (Wave 1)
  + ContactForm component  (Wave 1)
  + Product pages / Stripe (Wave 1)
      |
      v
templates.dreytools.com (NEW — Wave 3)
  - SaaS landing template
  - Info product template
  - Physical product template
  - ContactForm included
  - ProfileCard included

dashboard.dreytools.com (existing Life Dashboard)
  + Weather widget  (Wave 2)

drdrey.com (existing DREY AI Musician)
  + Music Player UI  (Wave 2)

dottie.dreytools.com (existing Dottie)
  + Web chat UI  (Wave 2)
  + Optional: wire into scheduling.dreytools.com (Wave 3)

scheduling.dreytools.com (NEW — Wave 3)
  - Full calendar
  - Event modals
  - Wires into Dottie phone booking

abs.dreytools.com (existing ABS Club)
  + Member chat  (Wave 2)
  + Metrics dashboard  (Wave 4 Option B)

1buttonbusiness.com (existing 1BB)
  + Task Management board  (Wave 4)
  + ContactForm  (Wave 1)
```

---

## Open Decisions — Drey's Call

1. **Chat UI first target:** Dottie web chat OR ABS Club community chat?
2. **Dashboard UI vertical:** G3AC / ABS Club / Viral Editz?
3. **Task Management:** Standalone practice first, or wait for 1BB Community Platform?
4. **Stack for new subdomains:** Convex + Next.js 16 (matches Life Dashboard) or Cloudflare Pages static where possible?

---

## Change Log
- [2026-04-17]: Created. Dave consolidation audit complete. 8 absorb / 2 new / 1 skip. By Claude + Dave.
