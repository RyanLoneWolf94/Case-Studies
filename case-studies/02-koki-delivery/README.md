# Koki Delivery — Cross-Border E-Commerce Platform (Lead Dev & DevOps)

> Built the original web e-commerce system for a cross-border marketplace bridging
> Chinese suppliers and Southern African consumers, then took over the entire platform
> as lead developer and DevOps — payment gateway integration, a full UI revamp, a
> rebuilt notification system, emergency infrastructure recovery, and ongoing app-store
> compliance.

| | |
|---|---|
| **Client** | Koki Technologies (Koki Delivery) |
| **Sector** | Cross-border e-commerce & logistics (China → Zimbabwe / South Africa) |
| **Agency** | LoneWolf Digital Inc. |
| **My role** | Lead Developer & DevOps Engineer |
| **Engagement type** | Initial build + ongoing platform ownership, maintenance & feature development |
| **Status** | 🔲 Ongoing — active support retainer |
| **Live** | [kokidelivery.co](https://www.kokidelivery.co) · Android app `com.koki.service` |

---

## 1. The Client & The Brief

Koki Technologies operates a **cross-border e-commerce and logistics marketplace** that
connects Chinese manufacturing suppliers with consumers in Southern Africa — primarily
Zimbabwe and South Africa. The platform has to do three hard things at once: run a
multi-vendor storefront, consolidate international freight through warehouse depots in
China, and settle payments across African mobile-money rails that most off-the-shelf
e-commerce systems have never heard of.

The engagement began with **building out the initial web e-commerce system** and has
since grown into **full platform ownership**: I act as Koki's lead developer and DevOps
engineer across their entire live ecosystem — web, mobile app, server infrastructure,
payments, and app-store presence.

**The core challenge:** keep a complex, revenue-generating cross-border platform stable,
compliant, and evolving — while re-architecting the pieces that were holding it back.

---

## 2. The System

Koki runs a multi-vendor marketplace stack that I maintain end to end:

```
[User App (Uni-App / Vue 2)] ──────┐
                                    ├──> [Huawei Cloud ECS (Nginx)] ──> [PHP / ThinkPHP] ──> [MySQL]
[Merchant Portal (Desktop Web)] ───┘
```

| Layer | Technology |
|---|---|
| Backend core | LikeShop Multi-Vendor (PHP 7.4/8.0, ThinkPHP) |
| Database | MySQL (transactional retail schema — baskets, vendor wallets, order queues) |
| Web server | Nginx reverse proxy + SSL/TLS termination |
| Mobile shell | Vue 2 compiled via Uni-App into a self-hosted Android APK (`com.koki.service`) |
| Infrastructure | Huawei Cloud ECS (CN East — Shanghai), Aliyun DNS + enterprise mail |
| Background jobs | Queue worker (Supervisor) + cron for async email & scheduled tasks |

**Custom extensions I own:**

- **Warehouse freight consolidation hub** — processes external parcels entering Koki's
  Shanghai depots; handles dimensional-weight breaks, volume multipliers, and Air vs.
  Sea routing tiers.
- **Freight calculator web app** — a standalone shipping-cost estimator embedded into the
  mobile app via webview.
- **Cross-border payment pipeline** — the mobile-money integration layer (below).

---

## 3. What I Built & Took Over

### 3.1 Payment gateway integration

Integrated a **cross-border payment pipeline** purpose-built for the Zimbabwean market,
where standard card-only checkout fails most buyers:

- **Paynow gateway integration** — synchronous API mappings for real-time processing of
  **EcoCash, OneMoney, Innbucks, and Zimswitch** bank cards.
- **Offline receipt / QR state machine** — an administrative validation loop that locks an
  order into a *"Pending Audit"* state until platform staff review a bank-payment
  screenshot uploaded by the customer, then releases it. This closes the gap for buyers
  paying by manual bank transfer, which is still common across the region.

### 3.2 UI revamp

Revamped the platform's user interface across the storefront and mobile shell to modernise
the buyer experience and tighten the in-app navigation — including the webview-embed
pattern used to surface custom tools (freight calculator, custom pages) cleanly inside the
native app without breaking the Uni-App routing.

### 3.3 Notification system

Rebuilt and hardened the seller **order-notification system** after diagnosing a
production failure where sellers stopped receiving order emails:

- **Root-caused** the failure to a background **queue worker** that was never restarted
  after an infrastructure outage — buyer inquiry emails kept working because they fire
  *synchronously*, while seller order notifications fire *asynchronously* through the
  queue. The behavioural split was the diagnostic key.
- **Fixed** the delivery path and **hardened** it so the worker survives future reboots
  (Supervisor enabled on boot), and documented the full-stack restart sequence so the
  outage can't silently recur.
- Verified the Aliyun enterprise-mail SMTP path end to end
  (`smtp.qiye.aliyun.com:465` SSL), including resolving a separate SMTP auth lock on the
  mail account.

### 3.4 DevOps & infrastructure recovery

Act as Koki's DevOps lead on live infrastructure. Headline incident:

- **INC-2026-051 — full platform blackout.** A hosting-account billing freeze triggered a
  hard shutdown on Huawei Cloud and **released the server's Elastic IP**, decoupling it
  from the public internet. I handled the complete recovery: **re-provisioned a fresh
  EIP**, rebound it to the server instance, restored firewall/SSH access, brought the
  **full stack back up in the correct order** (MySQL → PHP-FPM → Nginx → queue worker →
  cron), and **realigned the Aliyun DNS records** to the new IP to restore the domain.

---

## 4. App-Store Compliance & Lifecycle

Own Koki's mobile presence on **Google Play** (Koki Technologies org account) and the push
to iOS:

- **Target API level update** — recompiled the Uni-App build to meet Google's mandatory
  API-level policy, keeping the app publishable past the enforcement deadline.
- **Developer-account activity compliance** — resolved an inactivity-closure warning via a
  compliant submission (one action clearing two warnings).
- **iOS App Store** — preparing Koki's first App Store submission (signing, build, upload).

---

## 5. Deliverables

- 🛒 **Initial web e-commerce system** — multi-vendor marketplace build
- 💳 **Cross-border payment pipeline** — Paynow + EcoCash / OneMoney / Innbucks / Zimswitch, plus offline-receipt audit flow
- 🎨 **UI revamp** — storefront + mobile shell, with clean webview embedding
- 🔔 **Rebuilt notification system** — async order emails, root-caused, fixed, and hardened
- 📦 **Freight consolidation hub + calculator** — custom logistics extensions
- 🛠️ **DevOps ownership** — infrastructure recovery, full-stack restart runbooks, DNS/EIP management
- 📱 **App-store lifecycle** — Google Play compliance + iOS submission prep
- 📚 **Operational runbooks** — systems-architecture, incident, and engagement documentation for continuity

---

## 6. Process — Ownership Model

```
Initial build  →  Platform handover  →  Lead dev + DevOps ownership
     →  Payment integration  →  UI revamp  →  Notification rebuild
     →  Incident recovery (INC-2026-051)  →  App-store compliance  →  Ongoing retainer
```

Rather than a one-off project, this is an **ongoing ownership engagement**: I'm the single
point of accountability for Koki's live ecosystem under a support retainer, combining
hands-on development, infrastructure operations, and release management — and documenting
each system and incident into reusable runbooks so the platform stays maintainable.

---

## 7. Outcome

Koki moved from a system that was **built, then at risk of stalling** to a **stable,
compliant, actively maintained cross-border platform** with a payment layer tuned to its
real market, a modernised UI, a reliable notification system, and infrastructure that can
be recovered fast when things break. The engagement continues as an active retainer, with
the mobile footprint expanding to iOS and a longer-term platform modernisation on the
roadmap.

---

*Case study · LoneWolf Digital Inc. · Ryan Nyasha Makwabarara, Lead Developer & DevOps*
