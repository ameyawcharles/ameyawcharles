# Charles Ameyaw

**Full-stack developer · TypeScript, Next.js, PostgreSQL · Accra, Ghana**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-charles--ameyaw-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/charles-ameyaw-9a0469363)
[![Portfolio](https://img.shields.io/badge/Portfolio-dev.ameyawcharles.com-000000?style=flat-square)](https://dev.ameyawcharles.com)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)](https://supabase.com)

### 👋 About

I'm a full-stack developer who builds web applications where correctness matters: checkout, inventory, payments and multi-tenant platforms. I work mainly in TypeScript, Next.js and PostgreSQL, on Supabase.

My engineering philosophy centers on first-principles thinking: build systems that stay correct under concurrent load, enforce strict data consistency, and fail safely. Whether I'm designing a stock ledger that cannot oversell, an idempotent checkout, or tenant isolation with row-level security, my focus is reliability I can prove with tests, not just claim.

**Core stack**
- **Languages & frameworks:** TypeScript, JavaScript, React, Next.js, SQL (PL/pgSQL)
- **Data:** PostgreSQL, Supabase (row-level security)
- **Infrastructure & workflow:** Vercel, GitHub Actions CI, REST APIs, written design decisions (ADRs)
- **Payments & messaging:** Paystack, Moolre, Resend, Africa's Talking

I work well in asynchronous, remote-first settings: I write decisions down, keep changes small and reviewed, and let tests decide what ships.

📬 **Let's connect:** open to remote full-stack and backend opportunities. Find me on [LinkedIn](https://www.linkedin.com/in/charles-ameyaw-9a0469363).

**Top skills:** Full-Stack Development • PostgreSQL • TypeScript • Next.js • Database Design

### 📌 Start here: [pharmacy-stock-ledger](https://github.com/ameyawcharles/pharmacy-stock-ledger)

[![ci](https://github.com/ameyawcharles/pharmacy-stock-ledger/actions/workflows/ci.yml/badge.svg)](https://github.com/ameyawcharles/pharmacy-stock-ledger/actions/workflows/ci.yml)

A PostgreSQL stock ledger for pharmacies, extracted from a point-of-sale system I'm building.

- **It cannot oversell.** Rows are locked in a fixed order, so 300 concurrent sales against 100 units sell exactly 100.
- **A retry never double-charges.** Checkout takes an idempotency key; a replay returns the original sale.
- **Expiry is enforced, not displayed.** Sales draw from the batch expiring soonest, and expired batches are never sold.
- **History cannot be rewritten.** The ledger is immutable, and `verify_stock_integrity()` proves the numbers add up.
- **It's reviewable.** 84 checks run against a real PostgreSQL on every push, design decisions are written up as ADRs, and `main` is protected: every change goes through a pull request with a passing check.

### 🚀 Projects

| Project | What it is | Where it stands |
| --- | --- | --- |
| [**pharmacy-stock-ledger**](https://github.com/ameyawcharles/pharmacy-stock-ledger) | PostgreSQL stock ledger for pharmacies | Public, with CI |
| [**LaunchDrop**](https://launchdropp.com) | Marketplace for ready-made, SEO-optimized websites | Deployed. Paystack and Moolre payments, Resend email, Supabase row-level-security multi-tenancy, admin approval flow for listings |
| **PharmaPOS** | Point-of-sale and stock control for pharmacies in Ghana | Prototype. Stock ledger, batches and atomic checkout are built and tested; payments and offline selling are next |
| **ObiBot** | WhatsApp-first AI business advisor for Ghanaian SMEs | In development. Africa's Talking, Claude API and Supabase |

### 📫 Contact

Message me on [LinkedIn](https://www.linkedin.com/in/charles-ameyaw-9a0469363).
