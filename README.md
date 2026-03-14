# Oreel - Cosmetics & Fashion E-Commerce on Stellar Blockchain

![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)
![Next.js](https://img.shields.io/badge/Next.js-14-black)
![React Native](https://img.shields.io/badge/React%20Native-0.72-blue)
![Express](https://img.shields.io/badge/Express-4.18-green)
![Stellar](https://img.shields.io/badge/Stellar-SDK-purple)

## 🌟 Overview
Oreel is a revolutionary e-commerce platform for cosmetics and fashion products built on the **Stellar blockchain**. By leveraging blockchain technology, we provide transparent transactions, secure payments, and authentic product verification for the beauty and fashion industry.

## ✨ Key Features
* **Blockchain-Powered Payments:** Secure and transparent transactions using Stellar network
* **Multi-Platform Support:** Web (Next.js) and Mobile (React Native) applications
* **Real-Time Chat:** Integrated customer support and vendor communication
* **Product Authentication:** Verify product authenticity via blockchain
* **Smart Contracts:** Automated escrow and dispute resolution
* **Digital Asset Management:** Tokenized loyalty rewards and product ownership

## 🏗️ Project Structure
```
oreel/
├── oreel-web/                 # Next.js web application
├── oreel-mobile/              # React Native mobile app
├── oreel-backend/             # Express.js backend API
├── docs/                       # Documentation
├── contracts/                  # Stellar smart contracts
└── README.md                   # This file
```

## 🚀 Getting Started

### Prerequisites
* **Node.js 18+**
* **npm** or **yarn**
* **PostgreSQL 14+**
* **MongoDB 6+**
* **Redis** (for caching and real-time features)
* **Git**
* **Stellar account** (testnet for development)

### Quick Start
1. **Clone the repository**
   ```bash
    git clone https://github.com/yourusername/oreel.git
    cd oreel
  ```
2. **Install dependencies for all services**
```bash
    # Install web dependencies
    cd oreel-web && npm install

    # Install mobile dependencies
    cd ../oreel-mobile && npm install

    # Install backend dependencies
    cd ../oreel-backend && npm install
```

3. **Set up environment variables**
Copy the example environment files and configure them for each service:
```bash
# Backend
cp oreel-backend/.env.example oreel-backend/.env

# Web
cp oreel-web/.env.example oreel-web/.env.local

# Mobile
cp oreel-mobile/.env.example oreel-mobile/.env
```

4. **Start databases**
```bash
    # Using Docker (recommended)
    docker-compose up -d postgres mongodb redis

    # Or start services manually
```

5. **Run database migrations**
```bash
    cd oreel-backend
    npm run prisma:migrate
    npm run seed
```

6. **Start development servers**
```bash
    # Backend (from oreel-backend)
    npm run dev

    # Web (from oreel-web)
    npm run dev

    # Mobile (from oreel-mobile)
    npm start
```

## 💻 Development Guides

### Web Application (Next.js)
* **URL:** `http://localhost:3000`
* **Docs:** [Web README](./apps/web/README.md)
* **Tech Stack:** Next.js 14, Tailwind CSS, Zustand, React Query

### Mobile Application (React Native)
* **Run on iOS:** `npm run ios`
* **Run on Android:** `npm run android`
* **Docs:** [Mobile README](./apps/mobile/README.md)
* **Tech Stack:** Expo, React Navigation, NativeWind

### Backend API
* **URL:** `http://localhost:5000`
* **API Docs:** `http://localhost:5000/api-docs`
* **Docs:** [Backend README](./apps/api/README.md)
* **Tech Stack:** Express.js, Prisma, Mongoose, Socket.io


## 🤝 Contributing
We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Workflow
1. **Fork the repository**
2. **Create a feature branch**
```bash
    git checkout -b feature/amazing-feature
```
3. **Commit your changes**
```bash
git commit -m 'feat: add amazing feature'
```
4. **Push to the branch**
```bash
git push origin feature/amazing-feature
```

5. **Open a Pull Request**

## 🙏 Acknowledgments

* **Stellar Development Foundation**
* **Open source community**
* **All our contributors and supporters**

Built with ❤️ for the beauty, fashion and stellar communities









