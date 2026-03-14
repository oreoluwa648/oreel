# Oreel — Backend Service

Lightweight scaffold for the Oreel backend service (Express + TypeScript). This repository contains the folder structure and placeholders used to implement APIs, background jobs, sockets, and integrations (Prisma, Mongo, Redis, Stellar, Stripe, etc.).

## Quick Start

- Install dependencies:

```bash
cd oreel-backend
npm install
```

- Copy environment example and set secrets:

```bash
cp .env.example .env
# edit .env to set DATABASE_URL, MONGODB_URI, REDIS_URL, JWT_SECRET, etc.
```

- Prisma (if using Postgres):

```bash
npx prisma generate
npx prisma migrate dev --name init
node prisma/seed.js # or npm run prisma:seed
```

- Run in development:

```bash
npm run dev
```

## Folder Structure

Top-level overview of the scaffold (only files relevant to development shown):

```
oreel-backend/
├─ src/
│  ├─ api/
│  │  └─ v1/
│  │     ├─ controllers/        # Request handlers
│  │     ├─ routes/             # Express route definitions
│  │     ├─ middlewares/        # Route-level middleware
│  │     ├─ validations/        # Request schemas (Zod/Joi)
│  │     └─ dtos/               # Data-transfer objects
│  ├─ config/                   # DB, Redis, Stellar, email, env
│  ├─ modules/                  # Domain modules (auth, users, products...)
│  ├─ core/                     # Errors, utils, response helpers
│  ├─ middlewares/              # Global/infra middlewares
│  ├─ jobs/                     # Queues and workers
│  │  ├─ queues/
│  │  └─ workers/
│  ├─ sockets/                  # Socket.io handlers and middleware
│  ├─ types/                    # App-wide TypeScript types and defs
│  ├─ app.ts                    # App bootstrap
│  └─ server.ts                 # Server entry (listen)
├─ prisma/
│  ├─ schema.prisma
│  ├─ migrations/
│  └─ seed.ts
├─ scripts/                     # Helper scripts (seed, migrations)
├─ tests/
│  ├─ unit/
│  ├─ integration/
│  └─ e2e/
├─ logs/
└─ uploads/
```

## Environment Variables (examples)

- `DATABASE_URL` — Postgres connection string
- `MONGODB_URI` — MongoDB connection string
- `REDIS_URL` — Redis connection string
- `PORT` — Server port
- `NODE_ENV` — development | production
- `JWT_SECRET` — JWT signing secret
- `STELLAR_HORIZON_URL`, `STELLAR_NETWORK_PASSPHRASE` — Stellar config
- `STRIPE_SECRET_KEY` — Stripe secret for payments
- `SMTP_HOST`, `SMTP_USER`, `SMTP_PASS` — Email delivery

Adjust `.env.example` in this folder to reflect the required keys for your environment.

## Scripts (examples in package.json)

- `npm run dev` — Start dev server with nodemon/ts-node
- `npm run build` — Compile TypeScript
- `npm run start` — Start production build
- `npm run prisma:seed` — Seed the database


