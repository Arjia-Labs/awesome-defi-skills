# Awesome DeFi AI Skills [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI skills files, MCP servers, and agent toolkits that enable AI coding assistants and autonomous agents to interact with DeFi protocols, execute on-chain actions, and analyze blockchain data.

As of early 2026, there are **100+ blockchain-focused MCP servers** live and growing fast. This list focuses on the best tools for DeFi builders and traders.

## Contents

- [What Are Skills Files?](#what-are-skills-files)
- [Protocol Skills Files](#protocol-skills-files)
- [DeFi MCP Servers](#defi-mcp-servers)
- [Market Data MCP Servers](#market-data-mcp-servers)
- [Multi-Chain & Wallet MCP Servers](#multi-chain--wallet-mcp-servers)
- [Blockchain Analytics & Security](#blockchain-analytics--security)
- [Skills Marketplaces & Directories](#skills-marketplaces--directories)
- [Emerging Standards](#emerging-standards)
- [Contributing](#contributing)

---

## What Are Skills Files?

**Skills files** are structured knowledge documents that teach AI agents how to use specific tools and protocols. Install them via:

```bash
npx skills add <org>/<repo>
```

Once installed, the AI agent gains protocol-specific capabilities — from executing swaps to managing liquidity positions.

**Model Context Protocol (MCP)** is an open standard (championed by Anthropic, adopted by Microsoft, OpenAI, and Google) that connects AI models to external tools, APIs, and blockchains.

---

## Protocol Skills Files

Official and community-maintained skills packages from major DeFi protocols.

### 🦄 Uniswap AI
> **Official** — by Uniswap Labs

- **Repo:** [github.com/Uniswap/uniswap-ai](https://github.com/Uniswap/uniswap-ai)
- **Install:** `npx skills add Uniswap/uniswap-ai`
- **Stars:** 74+ | **License:** MIT

Seven open-source AI skills for building on Uniswap:
- `uniswap-hooks` — Uniswap v4 hook development utilities
- `uniswap-trading` — Swap integration and execution
- `uniswap-cca` — Cooperative custody auctions support
- `uniswap-driver` — Swap and liquidity planning tools
- `uniswap-viem` — EVM integration with viem and wagmi
- Security foundations — Guardrails to reduce execution mistakes
- Configurator/deployer — v4 hook deployment support

Also available: `/plugin marketplace add uniswap/uniswap-ai`

---

### ⛓️ BNB Chain Skills
> **Official** — by BNB Chain

- **Repo:** [github.com/bnb-chain/bnbchain-skills](https://github.com/bnb-chain/bnbchain-skills)
- **Install:** `npx skills add bnb-chain/bnbchain-skills`
- **Stars:** 51+ | **License:** MIT

AI agent skills for the BNB Chain MCP server:
- Query blocks and transactions
- Interact with smart contracts
- Manage tokens and NFTs
- Handle wallet operations
- Register agents via **ERC-8004**
- Manage **Greenfield** decentralized storage

---

### 🛡️ OpenZeppelin Skills
> **Official** — by OpenZeppelin

- **Repo:** [github.com/OpenZeppelin/openzeppelin-skills](https://github.com/OpenZeppelin/openzeppelin-skills)
- **Install:** `npx skills add OpenZeppelin/openzeppelin-skills`
- **License:** MIT

Nine AI skills covering secure smart contract development across multiple blockchain platforms:
- `develop-secure-contracts` — Create secure contracts using OpenZeppelin's audited libraries
- `setup-solidity-contracts` — Initialize a Solidity project
- `setup-cairo-contracts` — Initialize a Cairo project (StarkNet)
- `setup-stylus-contracts` — Initialize a Stylus project (Arbitrum)
- `setup-stellar-contracts` — Initialize a Stellar project
- `upgrade-solidity-contracts` — Manage Solidity contract upgrades safely
- `upgrade-cairo-contracts`, `upgrade-stylus-contracts`, `upgrade-stellar-contracts`

Also available: `/plugin marketplace add OpenZeppelin/openzeppelin-skills`

---

### 💧 Byreal CLI
> **Official** — by Byreal (Solana CLMM DEX)

- **Repo:** [github.com/byreal-git/byreal-cli](https://github.com/byreal-git/byreal-cli)
- **Install:** `npx skills add byreal-git/byreal-cli` or `npm i -g @byreal-io/byreal-cli`
- **Latest:** v0.2.6 (March 2026) | **License:** MIT

AI-native CLI for concentrated liquidity on Solana. Every command supports `-o json`:
- Pool management — List, search, K-line charts, APR/TVL/volume, risk analysis
- Position management — Open/close positions, claim fees, copy top farmers
- Trading — Preview swaps, execute with slippage control
- Token data — Search tokens, real-time prices
- AI-optimized — Recommends optimal position ranges automatically

---

### 🌐 Multichain Protocol (MeneseSDK on ICP)

- **Install:** `npx playbooks add skill openclaw/skills --skill multichain-protocol`
- **Chains:** 19 (Solana, Ethereum, Bitcoin, Arbitrum, Base, Polygon, BSC, Optimism, ICP, XRP, SUI, TON, Cardano, Aptos, NEAR, Tron, Litecoin, CloakCoin, THORChain)

Operate across 19 blockchains from a single ICP canister:
- DEX swaps (Raydium, Uniswap, ICPSwap, KongSwap, Cetus, Minswap)
- DeFi positions (Aave, Lido, LP management)
- Automated trading (DCA, stop-loss, rebalancing)
- Cross-chain bridging
- First 5 transactions free

---

## DeFi MCP Servers

Standalone MCP servers that connect AI agents to DeFi protocols.

### DeFi Trading MCP

- **Repo:** [github.com/edkdev/defi-trading-mcp](https://github.com/edkdev/defi-trading-mcp)
- **Install:** `npx defi-trading-mcp`
- **Chains:** 17+ (Base, Polygon, Arbitrum, Optimism, BSC, Avalanche, and more)

Autonomous crypto trading agent MCP server with:
- Portfolio management across all chains
- Memecoin opportunity scanner
- Technical analysis with pattern recognition
- **MEV protection** — private mempool routing on Ethereum
- **Gasless swaps** on supported chains
- Stop-loss execution, risk assessment, rebalancing

---

### DeFi Yields MCP (DefiLlama)

- **Repo:** [github.com/kukapay/defi-yields-mcp](https://github.com/kukapay/defi-yields-mcp)
- **Install:** `uvx defi-yields-mcp`
- **Data source:** DefiLlama

Explore DeFi yield opportunities across protocols:
- Filter yield pools by chain (Ethereum, Solana, etc.) or project (Lido, Aave, etc.)
- Analyze APY, 30-day mean APY, and yield predictions
- Predictive classification (Stable/Up/Down) with confidence scores
- [DefiLPKit](https://defilpkit.com) - Free read-only LP calculator: fee APR, estimated net yield after impermanent loss and gas, and range scenarios for Uniswap v3, PancakeSwap v3, Aerodrome and Raydium pools.

---

### GOAT — On-Chain Agent MCP

- **Tagline:** "One MCP to rule all chains"
- **Actions:** 200+ on-chain actions
- **Chains:** Ethereum, Solana, Base, and more

Fetch data and execute smart contract interactions across multiple chains from a single MCP server.

---

### Solana Agent Kit (SendAI)

- **Official Solana MCP server** (announced July 2025)
- **Actions:** 40+ Solana-specific actions

Full on-chain toolkit:
- Wallet management and balance queries
- Token swaps via Jupiter
- Token and NFT deployment
- Staking, limit orders, and DeFi operations
- Account, transaction, and network state queries

---

### deBridge MCP Server

- **Launched:** February 2026
- **Chains:** 24 networks (Ethereum, Solana, TRON, Base, etc.)

Cross-chain operations for AI agents:
- Cross-chain swaps and bridging
- MEV protection and optimized routing
- Automatic wallet management and transaction retries
- Zero TVL solver-driven architecture

---

### Agentipy (Solana)

- **Repo:** [github.com/niceberginc/agentipy](https://github.com/niceberginc/agentipy)
- **Language:** Python

Python framework with built-in MCP module for Solana:
- Balance checks, cross-chain swaps (deBridge)
- Pyth price feeds, CoinGecko analytics
- Jupiter integration for swaps
- AI-driven trading capabilities

---

## Market Data MCP Servers

MCP servers focused on crypto market data and analytics.

### 🦎 CoinGecko MCP Server

One of the most mature MCP products in crypto:
- Access to 15,000+ coins across 1,000+ exchanges
- On-chain DEX data across 200+ networks (via GeckoTerminal)
- Trending tokens, new listings, top gainers/losers
- Historical OHLCV data
- Project metadata, social links, contract addresses

---

### DexPaprika MCP Server

- Real-time data for **5M+ tokens** across 20+ blockchain networks
- Token prices and liquidity pool data
- Historical analytics and DEX statistics

---

### DexScreener MCP Server

- **Repo:** [github.com/openSVM/dexscreener-mcp-server](https://github.com/openSVM/dexscreener-mcp-server)
- Real-time data from thousands of DEXes across dozens of blockchains
- Whale tracking, arbitrage detection, liquidity analysis

---

### CoinMarketCap MCP

- Real-time prices, market cap, and volume data
- Standard MCP interface for any AI agent

---

## Multi-Chain & Wallet MCP Servers

### Web3 MCP (Strangelove Ventures)

Multi-chain MCP supporting **Ethereum, Solana, Cardano, THORChain, XRP, Bitcoin**, and more. Fetch balances, account data, and execute transactions.

### EVM MCP Server

Supports **30+ EVM-compatible blockchains** (Ethereum, Polygon, BSC, Arbitrum). Contract interactions, ERC-20 balance queries, ENS lookups.

---

## Blockchain Analytics & Security

### Heurist Mesh MCP

On-chain analytics, token metrics, and security insights for smart contracts.

### Etherscan MCP

Fetch Ethereum blockchain data — token balances, ENS lookups, contract interactions via Etherscan API.

---

## Skills Marketplaces & Directories

Discover and install more DeFi AI skills:

| Platform | URL | Notable DeFi Skills |
|----------|-----|---------------------|
| LobeHub Skills Marketplace | [lobehub.com/skills](https://lobehub.com/en/skills) | defi-integration (Uniswap, Aave, Compound, Curve) |
| OpenClaw Directory | [openclawdirectory.dev](https://www.openclawdirectory.dev/skills/defi) | DeFi protocol interactions, DEX aggregators |
| Skills.sh | [skills.sh](https://skills.sh) | software-crypto-web3, blockchain-defi |
| Playbooks | [playbooks.com/skills](https://playbooks.com/skills) | multichain-protocol, blockchain-defi |
| VoltAgent Awesome Skills | [github.com/VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | Curated list of Claude Code skills and plugins |
| Awesome Blockchain MCPs | [github.com/royyannick/awesome-blockchain-mcps](https://github.com/royyannick/awesome-blockchain-mcps) | Curated list of all blockchain MCP servers |
| MCP Market | [mcpmarket.com](https://mcpmarket.com) | DeFi MCP server with 12 tools, no API keys needed |
| MCPKit | [mcpkit.com](https://www.mcpkit.com) | defi-yields-mcp, alchemy-mcp-server |
| DeFi Agents API | [github.com/nirholas/defi-agents](https://github.com/nirholas/defi-agents) | 42 production-ready agent definitions for Web3 |

---

## Emerging Standards

### ERC-8004 — AI Agent Identity

Expected to go live with Ethereum's **Glamsterdam hard fork** (Q2 2026). Developed in collaboration with Google, Coinbase, and MetaMask:
- Gives AI agents on-chain digital identity
- Enables verifiable agent registration
- Part of BNB Chain Skills (already supported)

### Key Trends

- **Non-custodial MCP** — servers that craft transactions without access to private keys
- **TEE-backed agents** — hardware isolation (secure enclaves) for on-chain execution
- **Multi-agent systems** — specialized agents for analysis, trading, and risk management
- **MCP tokens** — economic models built around the MCP protocol (SkyAI, DeMCP)
- **Agent-to-agent payments** — autonomous micropayments between AI agents

---

## Quick Reference

| Project | Type | Chains | Install Command |
|---------|------|--------|-----------------|
| Uniswap AI | Skills | EVM | `npx skills add Uniswap/uniswap-ai` |
| BNB Chain Skills | Skills | BNB Chain | `npx skills add bnb-chain/bnbchain-skills` |
| Byreal CLI | Skills + CLI | Solana | `npx skills add byreal-git/byreal-cli` |
| OpenZeppelin Skills | Skills | EVM, StarkNet, Stylus, Stellar | `npx skills add OpenZeppelin/openzeppelin-skills` |
| DeFi Trading MCP | MCP Server | 17+ EVM chains | `npx defi-trading-mcp` |
| DeFi Yields MCP | MCP Server | Multi-chain | `uvx defi-yields-mcp` |
| Solana Agent Kit | MCP Server | Solana | See repo |
| GOAT MCP | MCP Server | Multi-chain | See repo |
| deBridge MCP | MCP Server | 24 networks | See repo |
| Multichain Protocol | Skills | 19 chains | `npx playbooks add skill openclaw/skills --skill multichain-protocol` |
| DeFi Integration (LobeHub) | Skills | EVM | `npx -y @lobehub/market-cli skills install san-npm-skills-ws-defi-integration` |

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Add new skills files, MCP servers, or directories
- Keep descriptions concise and accurate
- Verify that links are working before submitting
- Follow the existing format

---

*Last updated: March 2026 | Curated by [Arjia Labs](https://arjia.city)*
