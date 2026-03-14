# Oreel Mobile — React Native (Expo)

This directory contains the React Native mobile application scaffold for Oreel, built with Expo and using the file-based Expo Router.

Overview
--------
- Expo + React Native (recommended via Expo CLI)
- File-based routing via Expo Router under `src/app`
- Stellar integration entry points under `src/lib/stellar`
- Modular components in `src/components` and services in `src/services`

Scaffolded structure
--------------------
oreel-mobile/
├── assets/
│   ├── images/
│   │   ├── splash.png
│   │   ├── icon.png
│   │   └── adaptive-icon.png
│   ├── fonts/ (.gitkeep)
│   └── animations/ (.gitkeep)
├── src/
│   ├── app/ (Expo Router)
│   │   ├── (auth)/_layout.tsx, login.tsx, register.tsx, forgot-password.tsx
│   │   ├── (tabs)/_layout.tsx, index.tsx, shop/, cart.tsx, wishlist.tsx, profile.tsx
│   │   ├── (dashboard)/_layout.tsx, orders/, wallet.tsx, settings.tsx
│   │   ├── chat/_layout.tsx, index.tsx, [id].tsx
│   │   ├── checkout/_layout.tsx, shipping.tsx, payment.tsx, success.tsx
│   │   └── _layout.tsx, index.tsx
│   ├── components/ (ui/, layout/, forms/)
│   ├── lib/ (stellar/, api/, auth/, utils/, hooks/)
│   ├── store/
│   ├── services/ (stellar/, chat/, notification/)
│   ├── types/
│   ├── config/
│   └── styles/
├── .env
├── app.json
├── babel.config.js
├── tailwind.config.js
├── tsconfig.json
├── metro.config.js
├── package.json
└── README.md

Notes
-----
- All files created here are placeholders or `.gitkeep` to preserve folder structure — no implementation code was added.
- The project uses the Expo Router file conventions; screens live under `src/app` and are organized into route groups like `(auth)`, `(tabs)`, and `(dashboard)`.

Quick start (developer)
-----------------------
Prerequisites: Node.js 18+, Yarn or npm, Expo CLI installed globally

```bash
cd oreel-mobile
npm install
npm start
```

Contributing
------------
Please follow the repo-level CONTRIBUTING guide. Implement features in feature branches and add tests where appropriate.

Contact
-------
Open an issue or ping the maintainers for questions about mobile architecture or API contracts.
