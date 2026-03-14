# Oreel — Web (Next.js)

![Next.js](https://img.shields.io/badge/Next.js-14-black)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)

Overview
--------
The Oreel web application is a Next.js 14 frontend using the App Router. This directory contains public assets, application routes, UI components, and client-side integrations for the Oreel storefront.

Highlights
---------
- App Router-based layout and route groups for Marketing, Shop, Auth and Dashboard
- Stellar SDK integration points under `lib/stellar`
- Shadcn-style `components/ui` + `components/shared` and `components/forms`
- Placeholder pages and `.gitkeep` files added for an initial scaffold

Folder structure
----------------
```
oreel-web/
├── app/
│   ├── (marketing)/
│   │   ├── page.tsx
│   │   ├── about/page.tsx
│   │   └── contact/page.tsx
│   ├── (shop)/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── categories/[slug]/page.tsx
│   │   ├── categories/[slug]/_components/  (category components)
│   │   ├── products/[slug]/page.tsx
│   │   ├── products/[slug]/_components/    (product components)
│   │   ├── cart/page.tsx
│   │   ├── checkout/page.tsx
│   │   └── search/page.tsx
│   ├── (auth)/
│   │   ├── layout.tsx
│   │   ├── login/page.tsx
│   │   └── register/page.tsx
│   └── (dashboard)/
│       ├── layout.tsx
│       ├── page.tsx
│       └── profile/, orders/, wallet/, chat/...
├── public/
│   ├── images/
│   │   ├── products/
│   │   ├── brands/
│   │   └── ui/
│   ├── fonts/
│   ├── favicon.ico
│   ├── og-image.png
│   ├── robots.txt
│   └── sitemap.xml
├── components/
│   ├── ui/
│   ├── shared/
│   └── forms/
├── lib/
│   ├── stellar/
│   ├── api/
│   └── auth/
├── store/
├── types/
├── config/
├── app/layout.tsx
├── app/globals.css
├── providers.tsx
├── .env.local
├── .env.production
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json
```

Notes
-----
- This project uses the Next.js App Router (no `src/` directory). Route groups like `(marketing)` and `(shop)` are used for layout separation.
- The `admin` application is implemented as a separate app and is not included here.
- Many files are placeholders (`page.tsx`/`layout.tsx`) and `.gitkeep` were added to keep empty folders in git; implement real components and pages as you develop.

Quick start
-----------
Prerequisites: Node.js 18+, npm or yarn

Install dependencies and run in development:

```bash
cd oreel-web
npm install
npm run dev
```

Environment
-----------
Copy and configure environment files as needed:

```bash
cp .env.local.example .env.local
```

Build & Production
------------------
```bash
npm run build
npm run start
```

Contributing
------------
Contributions are welcome — follow the repository-level `CONTRIBUTING.md` and create feature branches for work specific to the web app.

Contact
-------
For questions about the frontend structure or to request shared APIs, open an issue or ping the maintainers.
