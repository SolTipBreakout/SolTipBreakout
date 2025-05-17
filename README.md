# SolTip: Cross-Platform Solana Tipping System

[![Hackathon Project](https://img.shields.io/badge/Hackathon-Altschool%20Breakout-blue)](https://earn.superteam.fun/listing/altschool-breakout-hackathon-track-or-superteam-nigeria-demo-day/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

SolTip is a cross-platform tipping system built on the Solana blockchain that enables seamless tipping and wallet management across multiple social platforms (Twitter, Discord, and Telegram). The platform allows users to send SOL and tokens to social media users as easily as interacting with them on their platforms.

## 🌐 Live Demos

- **Frontend Website**: [http://m0gkg8kswkcws00okgswgkg8.34.67.137.207.sslip.io/](http://m0gkg8kswkcws00okgswgkg8.34.67.137.207.sslip.io/)
- **API/Bot Server**: [http://u4008kw840kcsgsc4kwgo448.34.67.137.207.sslip.io/](http://u4008kw840kcsgsc4kwgo448.34.67.137.207.sslip.io/)

## 🤖 Social Bots

- **Telegram**: [@solTipping_bot](https://t.me/solTipping_bot)
- **Twitter**: [@ajweb3devjimoh](https://twitter.com/ajweb3devjimoh)

## 🏛️ Architecture Overview

SolTip is built with a microservices architecture consisting of three main components:

1. **Frontend (SolTipConnect)**
   - A modern, responsive web application
   - Built with React, TypeScript, and TailwindCSS
   - Provides user interface for wallet management, social account linking, and tipping

2. **MCP Endpoint (mcpendpoint)**
   - HTTP server exposing Model Context Protocol tools
   - Handles Solana blockchain integration
   - Manages wallet operations, transaction signing

3. **Bot Server**
   - Manages connections to social platforms (Twitter, Telegram, Discord)
   - Processes incoming commands from social platforms
   - Routes requests to the MCP Endpoint for blockchain operations

### System Flow

```
┌──────────────┐      ┌───────────────┐      ┌───────────────┐
│              │      │               │      │               │
│   Frontend   │<─────│  MCP Endpoint │<─────│   Bot Server  │
│              │      │               │      │               │
└──────────────┘      └───────────────┘      └───────────────┘
       ▲                      ▲                     ▲
       │                      │                     │
       ▼                      ▼                     ▼
┌──────────────┐      ┌───────────────┐      ┌───────────────┐
│              │      │               │      │               │
│    Users     │      │    Solana     │      │  Social Media │
│ (Web Browser)│      │  Blockchain   │      │   Platforms   │
│              │      │               │      │               │
└──────────────┘      └───────────────┘      └───────────────┘
```

## 🚀 Features

- **Cross-Platform Tipping**: Send SOL to users on Twitter, Discord, and Telegram
- **Wallet Management**: Create and manage Solana wallets through a simple interface
- **Social Account Linking**: Connect social accounts to your Solana wallet
- **Transaction History**: View all your tipping activities
- **Privy Authentication**: Simplified wallet authentication
- **Custodial and Non-Custodial Options**: Use your own wallet or create a managed one
- **Real-time Balance Updates**: See your wallet balance in real-time

## 💻 Key Technologies

- **Frontend**: React, TypeScript, TailwindCSS, Vite
- **Authentication**: Privy
- **Wallet Integration**: Solana Web3.js, Solana Wallet Adapter
- **API Integration**: React Query
- **Backend**: Express, TypeScript, Model Context Protocol
- **Blockchain**: Solana
- **Social Integrations**: Twitter API, Telegram Bot API, Discord Bot API

## 🛠️ Project Structure

```
.
├── SolTipConnect/       # Frontend application
├── mcpendpoint/         # Solana MCP HTTP server
│   └── ...              # See mcpendpoint/README.md for details
└── bot-server/          # Bot server for social platforms
```

Each component has its own README with detailed information:
- [Frontend README](./SolTipConnect/README.md)
- [MCP Endpoint README](./mcpendpoint/README.md)

## 🚀 Quick Start

### Prerequisites

- Node.js 16+
- pnpm
- Solana wallet (for development)

### Running the Project (Development)

1. Clone the repository
```bash
git clone https://github.com/SolTipBreakout/solBreakOut.git
cd solBreakOut
```

2. Set up the MCP Endpoint
```bash
cd mcpendpoint
pnpm install
pnpm dev
```

3. Set up the Frontend
```bash
cd ../SolTipConnect
pnpm install
pnpm dev
```

4. Set up environment variables for each component (see respective READMEs)

## 📝 Usage Examples

### Tipping via Telegram Bot
1. Start a chat with [@solTipping_bot](https://t.me/solTipping_bot)
2. Link your wallet: `/link_wallet <wallet_address>`
3. Tip another user: `/tip @username 0.1`

### Tipping via Web Interface
1. Log in to the [frontend](http://m0gkg8kswkcws00okgswgkg8.34.67.137.207.sslip.io/)
2. Connect your wallet
3. Link your social accounts
4. Use the Send Tip form to tip a user by their social handle

## 👥 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for details.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## 🔗 Links

- [GitHub Organization](https://github.com/SolTipBreakout)
- [Altschool Breakout Hackathon](https://earn.superteam.fun/listing/altschool-breakout-hackathon-track-or-superteam-nigeria-demo-day/) 
