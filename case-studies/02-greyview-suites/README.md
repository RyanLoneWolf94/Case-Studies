# Greyview Suites — Hospitality Brand & Booking Platform

> A full-stack engagement that unified two independent Harare lodges under a single
> boutique brand and shipped a multi-property booking platform with its own staff admin
> console — spanning strategy, visual identity, web + application build, and digital
> marketing.

| | |
|---|---|
| **Client** | Greyview Suites — hospitality group operating two lodges in Harare, Zimbabwe (Greyview Lodge, Belvedere · Serene Haven Lodge, Strathaven) |
| **Sector** | Hospitality / boutique lodging |
| **Agency** | LoneWolf Digital Inc. |
| **My role** | Creative Director, Brand Designer & Lead Developer |
| **Engagement type** | Brand strategy + visual identity + multi-property booking platform + digital marketing |
| **Project code** | GVS-001 |
| **Status** | 🔲 In progress — platform in final build, pre-launch |
| **Live** | [add live domain] |

---

## 1. The Client & The Brief

Greyview Suites came to LoneWolf Digital as **two separately-run lodges** — Greyview Lodge
in Belvedere and Serene Haven Lodge in Strathaven — with no shared brand, no online
booking, and guest enquiries handled ad-hoc over phone and WhatsApp.

Rather than scope this as a single-property website, the engagement was expanded to a
**unified multi-property platform**: one brand, one booking experience, and one staff
console that manages both lodges — with the architecture built so additional properties
can be added later without a rebuild.

**The core challenge:** build a credible, boutique-feeling hospitality brand *and* a real
booking system for the **Zimbabwe market** — where WhatsApp is the default communication
channel, international card processors like Stripe are unavailable, and local mobile money
(EcoCash) is how guests actually pay.

---

## 2. Discovery & Strategy

The strategy set three load-bearing decisions that shaped everything after:

- **One brand, two properties.** Greyview Lodge and Serene Haven Lodge were positioned as
  distinct properties under a single Greyview Suites umbrella — shared identity and booking
  flow, individual property pages and room catalogues.
- **WhatsApp-first, not an afterthought.** In this market WhatsApp is mandatory for guest
  and admin communication, so it was designed into the booking flow and the admin console
  from the start rather than bolted on.
- **Launch the core product first.** An OTA / partner-marketplace layer was validated
  conceptually but flagged as thin-margin and deliberately **deferred to Phase 2**, so the
  core booking product could ship first.

### Market & positioning
- **Market:** Harare, Zimbabwe — domestic and regional travellers
- **Positioning:** boutique / editorial hospitality — elevated above a generic lodge
  listing, approachable for a non-technical guest
- **Brand tagline:** [add tagline]

---

## 3. Visual Identity

The identity was built around an **editorial / boutique** direction — a serif-led,
hospitality-grade look rather than a utilitarian booking-site feel.

### Colour system

| Role | Colour | Hex |
|---|---|---|
| Anchor | Deep Navy-Teal | `#002834` |
| Primary (buttons) | Medium Teal | `#007F9E` |
| Accent | Light Cyan-Teal | `#29B6CC` |
| Secondary (buttons) | Kalahari Brown | `#B47C57` |
| WhatsApp (actions) | WhatsApp Green | `#1DA851` |

> The teal family anchors the brand; Kalahari Brown adds a warm, regional counterpoint.
> The WhatsApp green was deliberately **deepened from the stock `#25D366`** so white button
> text stays legible — a small accessibility call that recurs across the system.

### Typography
| Use | Typeface | Role |
|---|---|---|
| Headings | **Marcellus** (serif) | Editorial, boutique voice |
| Body / UI | **Hanken Grotesk** | Clean, legible interface text |

### UI language
- **Pill-shaped buttons** (`border-radius: 999px`) throughout
- Editorial layout with generous imagery and a boutique-hotel feel
- Full responsiveness across mobile, tablet, and desktop

### Logo & mark
- **Custom logo and brand mark** designed in-house for Greyview Suites
- [add logo concept / rationale — the idea the mark embodies]

---

## 4. Deliverables

A complete brand-and-platform package:

**Brand & identity**
- 🎨 **Brand system** — colour palette with roles + accessibility rules, typography
  pairing, button and UI language
- ✒️ **Custom logo & mark** for the unified Greyview Suites brand
- 🧭 **Brand/positioning strategy** — one-brand-two-properties structure, market definition,
  WhatsApp-first principle

**Platform**
- 🌐 **Guest-facing website — 5 pages:** homepage, two lodge property pages
  (Serene Haven, Greyview Lodge), a booking wizard, and a login-gated staff admin console
- 🧑‍💼 **Staff admin console** — manage bookings and both properties, with
  **four role tiers**: Owner·Admin, Admin, Manager, Receptionist
- 🗄️ **Supabase backend** — five-table schema, Row-Level Security, storage buckets, live
  website ↔ admin sync
- 💳 **Payments** — EcoCash via the ZB "Smile & Pay" gateway (Stripe excluded for the market;
  DPO Group / PesePay evaluated)
- 💬 **WhatsApp integration** — booking and admin actions wired to the business line
- 🤖 **AI concierge (planned)** — language-only assistance in **draft-don't-send** mode;
  all booking and availability logic stays in deterministic code, never the AI
- 🖼️ **Photo asset pipeline** — room photos shortlisted, converted to WEBP at 1920px, and
  mapped to room categories across both lodges
- 📘 **Developer handoff documentation** — data model, website↔admin sync, integration
  checklist, and the full design system

**Marketing**
- 📣 **Digital marketing** — [add channels run, campaign focus, and any results/metrics]

---

## 5. Process — Client Interaction to Delivery

```
Client interaction  →  Discovery & strategy  →  Brand & identity  →  Static prototype (5 pages)
      →  Client approval  →  Full-stack build (Next.js + Supabase)  →  Payments & WhatsApp
      →  Photo pipeline  →  Admin console & roles  →  UI hardening  →  Launch
      →  Digital marketing
```

**Build approach:** an approved **five-page static HTML/CSS/JS prototype** (homepage, both
lodge pages, booking wizard, admin console) was ported to a production **Next.js 14 +
Supabase** application with live data — prototype first for fast client sign-off, then
engineered up to production.

**How the work was divided:** strategy, brand, front-end, back-end, payment integration,
and marketing were all run in-house as a single end-to-end engagement, with the client as
project owner and approver at each stage.

**Review pattern:** decisions were staged — prototype approval before the full build, and
options presented at key points rather than single take-it-or-leave-it recommendations.

---

## 6. Outcome

Greyview Suites moved from **two disconnected lodges with no online booking** to a single
boutique brand on a **unified, multi-property platform** — guest website, real booking
flow, a role-based staff admin console, local payments, and WhatsApp built in — architected
so more properties can be added without a rebuild, with an OTA/marketplace layer staged for
Phase 2.

- **Starting point:** no shared brand, no online booking, ad-hoc enquiries
- **Delivered:** brand system + custom logo, 5-page site, admin console, Supabase backend,
  EcoCash payments, WhatsApp integration, and a documented developer handoff
- **Results:** [add launch date, booking volume, marketing metrics once live]

---

*Case study · LoneWolf Digital Inc. · Ryan Nyasha Makwabarara, Creative Director*
