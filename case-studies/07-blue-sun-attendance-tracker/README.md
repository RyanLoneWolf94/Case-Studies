# Blue Sun Attendance Tracker — Single-File Classroom App

> A lightweight, bilingual attendance tracker for a Montessori school — a single HTML file
> with a full teacher workflow, admin-gated sign-off, and per-teacher reporting, built to
> run with zero installation.

| | |
|---|---|
| **Client** | Blue Sun Montessori |
| **Sector** | Early-childhood education |
| **Agency** | LoneWolf Digital Inc. |
| **My role** | Developer |
| **Engagement type** | Internal tool — single-file web app |
| **Status** | ✅ Delivered (prototype build) |

---

## 1. The Client & The Brief

Blue Sun Montessori needed a simple, reliable way to take and confirm **daily class
attendance** across a bilingual (Vietnamese / English) teaching environment — something
teachers could use immediately, without an install, an account system, or training.

**The core challenge:** fit a complete, trustworthy attendance workflow — marking,
teacher identity, locking, and reporting — into a tool light enough to run from a single
file.

---

## 2. The Build

The app is a **single self-contained HTML file** — no build step, no dependencies to
install, nothing to deploy to a server for the prototype. Everything the classroom needs
is in one file that just opens.

### Features
- 🌏 **Bilingual labels** — Vietnamese / English throughout
- 📅 **Month picker** — navigate and record across the month
- 👩‍🏫 **Teacher identity selector** — the active teacher is chosen up front
- ✍️ **Per-row teacher assignment** — each record can be attributed to a specific teacher
- 🔒 **Admin PIN-gated confirmation & locking** — attendance is confirmed and locked behind
  an admin PIN, so records cannot be changed after sign-off
- 📊 **Per-teacher summary table** — attendance rolled up by teacher

---

## 3. Technical Note & Path to Production

The prototype uses **Claude's `window.storage` API** for persistence, which works inside
Claude's environment. For **standalone deployment** — running on the school's own devices,
independently — the persistence layer would be swapped to **Supabase**, giving shared,
multi-device storage and a proper backend while keeping the same single-page interface.

This is a deliberate, documented upgrade path: ship a working tool now, with a clear route
to a production-grade backend when the school is ready to deploy it beyond the prototype.

---

## 4. Deliverables

- 🧩 **Single-file HTML attendance app** — zero-install, runs on open
- 🌏 **Bilingual (VI/EN) interface**
- 🔐 **Admin PIN sign-off & record locking**
- 📊 **Per-teacher summary reporting**
- 🛣️ **Documented production path** — swap `window.storage` → Supabase for standalone use

---

## 5. Outcome

Blue Sun Montessori got a **working, bilingual attendance tool** that any teacher can use
immediately and that an admin can lock down for integrity — delivered as a single file with
no setup. It stands as a compact example of fitting a complete, real-world classroom
workflow into the lightest possible package, with a clear, pre-planned route to a
multi-device production version.

---

*Case study · LoneWolf Digital Inc. · Ryan Nyasha Makwabarara, Developer*
