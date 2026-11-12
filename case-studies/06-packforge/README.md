# Packforge (The Nexus) — Studio Management SaaS

> A white-label project-management and client-portal SaaS, built to replace per-client
> dashboard coding with one reusable platform — client management, projects and tasks,
> quotes and invoices, contracts with digital signing, and an embedded AI assistant.

| | |
|---|---|
| **Client** | LoneWolf Digital Inc. (internal product) |
| **Sector** | B2B SaaS — agency/studio operations |
| **Agency** | LoneWolf Digital Inc. |
| **My role** | Product Owner, Architect & Developer |
| **Engagement type** | Full-stack SaaS product design & development |
| **Status** | 🔲 In active development |
| **Repo** | [github.com/RyanLoneWolf94/Packforge](https://github.com/RyanLoneWolf94/Packforge) · admin portal at `portal.lonewolfdigitech.com/admin` |

---

## 1. The Problem

Every client engagement at the studio had been getting its **own hand-coded dashboard** —
a progress tracker, a sign-off flow, a brand snapshot — rebuilt from scratch each time.
That does not scale. Packforge is the answer: **one reusable, white-label platform** that
runs studio operations and gives every client a portal, so the studio stops re-coding the
same thing per project.

**The core challenge:** consolidate studio management (clients, projects, money, documents)
into a single product that is reusable across every client, yet white-label enough to feel
like each client's own portal.

---

## 2. Product Scope

A full studio-operations suite:

- **Client management** — a single source of truth for every client
- **Project & task tracking** — status pipelines across projects
- **Quotes & invoices** — commercial documents generated in-platform
- **Time tracking**
- **Support tickets**
- **Contracts with digital signing**
- **Embedded AI assistant** — an in-app helper for studio and client workflows

---

## 3. Design System

| Token | Value |
|---|---|
| Sidebar | Deep Navy `#16123A` |
| Accent | Orange `#F47B20` |
| Content area | Soft Blue-Grey `#F0F2F8` |
| Cards | White |
| Typography | **Plus Jakarta Sans** |

A calm, professional admin aesthetic — a deep navy frame around a light working canvas,
with a single warm accent — so the product reads as a serious operations tool, not a toy.

---

## 4. Architecture & The Stack Pivot

Packforge went through a deliberate **platform pivot** as the product matured:

| Layer | Initial | Pivoted to |
|---|---|---|
| Frontend | React + Vite | React + Vite |
| Backend / DB | Supabase | **Firebase (Firestore)** |
| AI assistant | Claude / Anthropic ("Varka") | **Gemini** |
| Product brand | Packforge | **"The Nexus"** |

The **Firebase blueprint** defines three Firestore collections (**Profiles, Projects,
Tasks**), **four user roles**, and project status pipelines. Confirmed libraries include
**Recharts/D3** (reporting), **jsPDF** (document export), **react-signature-canvas**
(contract signing), and **Framer Motion** (interface motion). A complete build prompt
covering the full stack, design system, and database schema was produced to drive
scaffolding.

A **custom MCP server** was also built for Packforge client management, connecting the
platform's client operations into an AI-tooling workflow.

---

## 5. Deliverables

- 🏗️ **Full-stack SaaS application** — React/Vite front end, Firebase/Firestore backend
- 🎨 **Design system** — tokens, typography, component aesthetic
- 🗃️ **Data model** — Firestore collections, four roles, status pipelines
- 🧾 **Commercial tooling** — quotes, invoices, contracts with digital signing (jsPDF, signature canvas)
- 📊 **Reporting** — Recharts/D3 dashboards
- 🤖 **Embedded AI assistant** + a **custom MCP server** for client management
- 📋 **Full build prompt** — complete stack, design system, and schema specification

---

## 6. Outcome

Packforge turns a recurring cost — a bespoke dashboard per client — into a **single
reusable product**. It consolidates the studio's whole operational surface (clients,
projects, money, documents, support) behind one white-label platform with a client portal,
an AI assistant, and digital contract signing. As an internal product it also becomes a
**portfolio-grade SaaS build** in its own right, demonstrating full-stack architecture, a
considered design system, and a pragmatic mid-build platform pivot.

---

*Case study · LoneWolf Digital Inc. · Ryan Nyasha Makwabarara, Product Owner & Developer*
