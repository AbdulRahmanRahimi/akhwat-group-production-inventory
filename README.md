# Akhwat Group: Production & Inventory System

> **Client project** · Built by [Rahimi Tech Solution](https://github.com/AbdulRahmanRahimi) · The source code is private to the client.

A production, inventory and quality-control system for **Akhwat Group**, a veterinary medicine manufacturer and raw-material trader in Jalalabad, Afghanistan. Staff use it every day for purchasing, stock, sales, quality control and production costing.

## Modules

| Module | What it does |
|---|---|
| **Raw Materials** | Purchases in AFN or USD, stock tracked by lot and expiry (FEFO), multi-line sales with live margin, supplier and customer accounts with balances in each currency |
| **Quality Control** | Review queue for every sale with automatic checks (expired or near-expiry lots, below-cost prices, customer balance), approve or return with remarks, live notifications |
| **Production** | Production batches with formulations; raw materials drawn from stock lot by lot at their actual cost; finished goods by size and lot |
| **Costing** | Batch cost = materials at lot cost + expenses, spread over product sizes by content (per L, kg or tablet), with suggested prices from target margins |
| **Dashboards** | Stock value, low and expiring stock, sales and gross profit, payables and receivables, production output and cost per unit |

## Engineering highlights

- **Roles and permissions** (Owner, Raw Materials, Quality Control, Production) enforced with PostgreSQL Row Level Security
- **Audit log** and no-delete rules: corrections are recorded, never erased
- **Exact figures**: every number is computed live from the database, and the app shows an error rather than an invented value
- **Automated tests** run every migration against an in-process Postgres and check roles, RLS, the stock ledger, unit conversion, rounding and invoice numbering
- **Internationalised** with next-intl

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | Next.js 16 (App Router), TypeScript, Tailwind CSS 4, next-intl |
| Backend | Supabase: PostgreSQL, Auth, Storage, Realtime, Row Level Security |
| Hosting | Vercel |

---

Designed, built and deployed by **Abdul Rahman Rahimi**.
