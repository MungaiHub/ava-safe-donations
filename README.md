# 🚀 Avalanche Spark Launch - Crowdfunding DApp

A complete decentralized crowdfunding application built on Avalanche C-Chain with React frontend, Express backend, and Solidity smart contracts.

## ✨ Features

- 🏗️ **Create Campaigns** - Launch crowdfunding campaigns with AVAX goals
- 💰 **Support Projects** - Contribute AVAX to campaigns you believe in
- 🎯 **Goal-Based Funding** - Automatic fund distribution when goals are reached
- 💳 **Refund System** - Automatic refunds if campaigns don't reach their goals
- 👤 **User Profiles** - Track campaigns you've created and backed
- 🔍 **Search & Filter** - Find campaigns by category, creator, or keywords
- ⛓️ **Blockchain Verified** - All transactions on Avalanche C-Chain

## 🛠️ Quick Start

### Prerequisites
- Node.js v18+
- MetaMask wallet
- Test AVAX from [Fuji Faucet](https://faucet.avax.network/)
- MongoDB

### Installation

```bash
# Install dependencies
npm install --legacy-peer-deps
cd backend && npm install && cd ..

# Configure environment
cp .env.example .env
# Edit .env with your private key

# Deploy smart contracts
npx hardhat run scripts/deploy.ts --network fuji

# Update factory address in .env
# VITE_FACTORY_ADDRESS=0x... (from deployment)

# Start backend
cd backend && npm run dev

# In another terminal, start frontend
npm run dev
```

Visit http://localhost:5173

## 📚 Documentation

- **[NEXT_STEPS.md](./NEXT_STEPS.md)** - Start here! Step-by-step action plan
- **[SETUP_GUIDE.md](./SETUP_GUIDE.md)** - Comprehensive setup instructions
- **[DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md)** - Testnet & mainnet deployment
- **[QUICK_REFERENCE.md](./QUICK_REFERENCE.md)** - Commands cheat sheet
- **[IMPLEMENTATION_SUMMARY.md](./IMPLEMENTATION_SUMMARY.md)** - What was built
- **[PROJECT_INDEX.md](./PROJECT_INDEX.md)** - File listing & structure

## 🏗️ Architecture

```
Frontend (React/TypeScript)
    ↓
Web3 Services (Ethers.js)
    ↓
Smart Contracts (Avalanche)

Backend (Express/TypeScript)
    ↓
MongoDB
```

## 📁 Project Structure

```
avalanche-spark-launch/
├── contracts/              # Smart contracts
├── scripts/               # Deployment scripts
├── backend/               # Express API
├── src/                   # React frontend
└── docs/                  # Documentation
```

## 🔌 Tech Stack

### Frontend
- React 18 + TypeScript
- Vite
- Tailwind CSS + shadcn/ui
- Ethers.js v6
- React Router

### Backend
- Node.js + Express
- TypeScript
- MongoDB + Mongoose
- CORS

### Smart Contracts
- Solidity 0.8.20
- Hardhat
- Avalanche C-Chain

## 💻 Available Scripts

```bash
# Frontend
npm run dev           # Start dev server
npm run build        # Build for production
npm run lint         # Run ESLint

# Backend
cd backend && npm run dev      # Start backend dev
cd backend && npm run build    # Build backend
cd backend && npm run start    # Run production

# Smart Contracts
npm run hardhat:compile           # Compile
npm run hardhat:deploy:fuji       # Deploy to testnet
npm run hardhat:deploy:avax       # Deploy to mainnet
npm run hardhat:test             # Run tests

# Full Stack
npm run dev:all   # Start backend and frontend
```

## 🌐 Networks

### Fuji Testnet
- **Chain ID**: 43113
- **RPC**: https://api.avax-test.network/ext/bc/C/rpc
- **Explorer**: https://testnet.snowtrace.io/
- **Faucet**: https://faucet.avax.network/

### Avalanche Mainnet
- **Chain ID**: 43114
- **RPC**: https://api.avax.network/ext/bc/C/rpc
- **Explorer**: https://snowtrace.io/

## 📋 API Endpoints

### Campaigns
- `GET /api/campaigns` - List campaigns
- `GET /api/campaigns/:address` - Get campaign
- `POST /api/campaigns` - Create campaign

### Users
- `GET /api/users/:address` - Get profile
- `POST /api/users` - Create/update user
- `PUT /api/users/:address` - Update profile

[Full API docs](./SETUP_GUIDE.md#api-endpoints)

## 🔒 Security

- Private keys stored in environment variables
- CORS enabled for frontend communication
- Contract validation on all functions
- Event logging for transactions
- Emergency refund mechanisms

## 🧪 Testing

```bash
# Backend tests (when added)
cd backend && npm test

# Contract tests
npx hardhat test
```

## 📈 Performance

- Campaign metadata stored off-chain
- MongoDB indexing for fast queries
- Optimized gas usage in contracts
- Responsive UI with React Query

## 🚀 Deployment

For production deployment:

1. Read [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md)
2. Deploy contracts to mainnet
3. Configure production environment
4. Deploy frontend to CDN/hosting
5. Deploy backend to VPS/cloud

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repo
2. Create feature branch
3. Commit changes
4. Push and create PR

## 📝 License

MIT

## 🆘 Support

- **Stuck?** → Read [NEXT_STEPS.md](./NEXT_STEPS.md)
- **Questions?** → Check [QUICK_REFERENCE.md](./QUICK_REFERENCE.md)
- **Issues?** → See [SETUP_GUIDE.md](./SETUP_GUIDE.md#troubleshooting)

## 🎯 Roadmap

- ✅ Campaign creation
- ✅ AVAX contributions
- ✅ Refund mechanism
- 🔄 Multi-sig wallets
- 🔄 NFT rewards
- 🔄 Milestone-based releases
- 🔄 Dispute resolution
- 🔄 Mobile app

## 📞 Contact

- GitHub Issues: [Report bugs](https://github.com/MungaiHub/ava-safe-donations/issues)
- Email: amosmungai085@gmail.com---

**Ready to launch?** Start with [NEXT_STEPS.md](./NEXT_STEPS.md) 🚀
