# Londri 🧺

> Built as a submission for the [Nomba Hackathon](https://devcareer.io/programs/nomba-hackathon).

Londri is a management platform that gives independent laundry businesses a digital home. Providing services like: KYB-verified accounts, digital price lists, subscription plans, and a full order management workflow for both online bookings and walk-in customers. Payments are collected and reconciled through **Nomba** (checkout order and subscription based), and customers are kept updated at every step. It also provides a public-facing side for customers to discover nearby laundries, book pickups without creating an account, pay online, and (optionally) track orders and manage subscriptions from an authenticated dashboard.

## Live Demo

- **Frontend:** https://londri-prototype.vercel.app
- **Backend / API docs:** https://londri-backend.fastapicloud.dev/docs


---

## Repositories

This repo uses Git submodules. Clone with:

```bash
git clone --recurse-submodules <repo-url>
```

| Submodule | Stack | Directory |
|---|---|---|
| Frontend | Next.js + Tailwind CSS | `/londri_frontend` |
| Backend | FastAPI + PostgreSQL | `/backend` |

If you've already cloned without `--recurse-submodules`, run:

```bash
git submodule update --init --recursive
```

---

## Core Features

- Laundry owner onboarding with KYB verification
- Digital price list and subscription plan management
- Order tracking with a defined status workflow (online + walk-in)
- Nomba-powered payments — virtual counter accounts, payment links, and daily transaction reconciliation
- WhatsApp notifications at every order and payment milestone
- Public customer-facing landing page with location-based laundry discovery
- Guest booking (name, WhatsApp, email — no account needed)
- Customer dashboard for order history and subscription management

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, Tailwind CSS |
| Backend | FastAPI (Python), PostgreSQL, Redis, PostGIS |
| Payments | [Nomba API](https://developer.nomba.com) |
| Messaging | Twilio |
| Background Jobs | BackgroundTasks in FastAPI |
| Auth | JWT + OTP (passwordless for customers) |

---

## Getting Started

Refer to each submodule's own `README.md` for setup instructions:

- [`/londri_frontend`](./frontend/README.md) — environment variables, dev server, build
- [`/backend`](./backend/README.md) — virtual environment, database setup, running the API