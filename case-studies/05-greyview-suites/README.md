# Greyview Suites — Hotel Management System

> A multi-property hotel management system, re-architected from a browser-only prototype
> into a real multi-user application: a Supabase backend, role-based access across four
> tiers, and local mobile-money payments wired in through edge functions.

| | |
|---|---|
| **Client** | Greyview Suites |
| **Sector** | Hospitality — multi-property lodging |
| **Agency** | LoneWolf Digital Inc. |
| **My role** | Lead Developer & Systems Architect |
| **Engagement type** | Web application build + backend migration + payments integration |
| **Status** | 🔲 Ongoing — build & migration in progress |
| **Properties** | Serene Haven Lodge · Greyview Lodge |

---

## 1. The Client & The Brief

Greyview Suites operates **more than one property** (Serene Haven Lodge and Greyview
Lodge) and needed a single administrative system to run them. The starting point was a
front-end dashboard that kept its data in the browser's `localStorage` — fine for a
prototype, but unworkable for a real business: data lived on one device, could not be
shared between staff, and had no security model.

**The core challenge:** turn a single-device prototype into a **real multi-property,
multi-user system** — shared data, proper roles, and working local payments — without
throwing away the existing front end.

---

## 2. The System

### Backend migration
The core of the engagement is migrating the admin dashboard from **`localStorage` to
Supabase (PostgreSQL)** — moving from device-bound state to a shared, secured, cloud
database. The migration plan is deliberately full-scope, covering:

- a **five-table schema**
- **Row-Level Security (RLS)** policies
- **Storage bucket** setup for media/assets

### Role model
Access is organised into **four role tiers**, so each staff level sees and does only what
it should:

| Tier | Scope |
|---|---|
| **Owner · Admin** | Full control across all properties |
| **Admin** | Administrative management |
| **Manager** | Property-level management |
| **Receptionist** | Front-desk / day-to-day operations |

### Payments
**EcoCash** payment integration via **ZB Smile & Pay**, implemented with **Supabase Edge
Functions** — bringing Zimbabwe's dominant mobile-money rail directly into the booking and
billing flow rather than relying on off-platform payment.

---

## 3. Engineering Approach

A conscious concern throughout the build was **efficiency** — both of the system and of
the development process itself. Model selection and session structure were managed
deliberately to keep token/subscription cost down across a long-running build (with a
lighter model set as the default for routine implementation work and heavier reasoning
reserved for architecture decisions).

The build reuses the existing front end and layers a production backend beneath it, rather
than rewriting the interface — migration, not replacement.

---

## 4. Deliverables

- 🗄️ **Supabase (PostgreSQL) backend** — five-table schema
- 🔐 **Role-based access control** — four tiers, enforced with RLS policies
- 📦 **Storage buckets** for media and assets
- 💳 **EcoCash payments** via ZB Smile & Pay, through Supabase Edge Functions
- 🏨 **Multi-property admin dashboard** covering both lodges
- 🔄 **Migration path** from `localStorage` prototype to cloud database

---

## 5. Process — Prototype to Production

```
localStorage prototype  →  Schema design (5 tables, 4 roles)  →  Supabase migration
   →  RLS policies & storage buckets  →  EcoCash / ZB Smile & Pay via edge functions
   →  Multi-property admin dashboard
```

The work is structured as a migration: take a functioning but device-bound front end,
design the data model and security underneath it, move the data into Supabase, and wire in
the pieces a real hotel operation needs — roles and local payments — property by property.

---

## 6. Outcome

Greyview Suites is moving from a **single-device prototype to a secured, multi-user,
multi-property platform**: shared cloud data, four enforced role tiers, storage for
assets, and local EcoCash payments built directly into the system. The result is an admin
backbone both lodges can run on, with a security model and payment rail suited to the
Zimbabwean market.

---

*Case study · LoneWolf Digital Inc. · Ryan Nyasha Makwabarara, Lead Developer*
