
<p align="center">
  <img src="https://raw.githubusercontent.com/neilyan/awesome-selfhosted-crypto-pay/main/assets/logo.svg" width="200" alt="Awesome Self-Hosted Crypto Pay">
</p>

<h1 align="center">Awesome Self-Hosted Crypto Pay <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a></h1>

<p align="center">
  <strong>English</strong> | <a href="README.zh.md">中文</a>
</p>

> A curated list of **self-hosted cryptocurrency payment gateways, processors, and infrastructure** — open-source software you run on your own servers to accept crypto payments without third-party fees or custody.

Self-hosting a crypto payment gateway means **no monthly fees, no per-transaction cuts, no KYC, and full control of your private keys.** Your customers' payments go directly to your wallet.

This list covers Bitcoin/Lightning solutions, stablecoin processors, multi-rail orchestration layers, and everything in between.

---

## Contents

- [Featured](#featured)
- [Full-Stack Payment Gateways](#full-stack-payment-gateways)
- [Bitcoin & Lightning Network](#bitcoin--lightning-network)
- [Stablecoin Payment Solutions](#stablecoin-payment-solutions)
- [Payment Orchestration & Multi-Rail](#payment-orchestration--multi-rail)
- [Libraries & SDKs](#libraries--sdks)
- [Plugins & CMS Integrations](#plugins--cms-integrations)
- [Utilities & Tools](#utilities--tools)
- [Resources & Guides](#resources--guides)
- [Comparison Table](#comparison-table)
- [Contributing](#contributing)
- [License](#license)

---

## Featured

### XPayLabs

[![GitHub stars](https://img.shields.io/github/stars/neilyan/XPayLabs-java?style=flat-square)](https://github.com/neilyan/XPayLabs-java)
[![GitHub license](https://img.shields.io/github/license/neilyan/XPayLabs-java?style=flat-square)](https://github.com/neilyan/XPayLabs-java/blob/main/LICENSE)

**XPayLabs** — Zero-fee, self-hosted, non-custodial stablecoin payment gateway. Accept USDT, USDC, DAI, and BUSD on TRON (TRC-20), EVM chains (Ethereum, BSC, Polygon, Arbitrum, Optimism, Base, Avalanche), and SUI.

- **Zero fees** — no per-transaction charges, only blockchain gas (~$0.01 TRON)
- **Non-custodial** — private keys generated and stored in your Docker containers
- **White-label checkout** — fully customizable Vue 3 payment page, no third-party branding
- **Real-time mempool detection** — 1–6 second transaction confirmation
- **First-party SDKs** — Node.js/TypeScript (`@xpaylabs/node-sdk`) and Java/Spring Boot (`xpay-java-sdk`)
- **HMAC-SHA256 webhooks** with exponential backoff retry
- **Merchant dashboard** — Vue 3 admin panel with ECharts analytics
- **Deployment** — `docker compose up -d`, Kubernetes-ready
- **Pricing** — Free (MIT), optional support plans from $1,500

[Source Code](https://github.com/neilyan/XPayLabs-java) · [Website](https://xpaylabs.com) · [Docs](https://docs.xpaylabs.com) · [Demo](https://github.com/neilyan/XPayLabs-demo-vue) · [Node SDK](https://github.com/neilyan/XPayLabs-node-sdk) · [Java SDK](https://github.com/neilyan/XPayLabs-java-sdk)

---

## Full-Stack Payment Gateways

Complete, production-ready payment gateways you can deploy on your own infrastructure.

### BTCPay Server

[![GitHub stars](https://img.shields.io/github/stars/btcpayserver/btcpayserver?style=flat-square)](https://github.com/btcpayserver/btcpayserver)

The most mature self-hosted Bitcoin payment processor. Supports on-chain Bitcoin, Lightning Network (LND, CLN, Eclair), and Liquid. Multi-tenant, invoicing, POS app, crowdfunding, and donation pages.

- **Fees:** 0% (network fees only)
- **Custody:** Non-custodial
- **Focus:** Bitcoin, Lightning, Liquid
- **Deployment:** Docker, manual
- **Stack:** C#, .NET
- **License:** MIT

[Source Code](https://github.com/btcpayserver/btcpayserver) · [Website](https://btcpayserver.org) · [Docs](https://docs.btcpayserver.org)

---

### SHKeeper

[![GitHub stars](https://img.shields.io/github/stars/vsys-host/shkeeper.io?style=flat-square)](https://github.com/vsys-host/shkeeper.io)

Self-hosted cryptocurrency payment gateway supporting Bitcoin, Ethereum, USDT, and other tokens. Integrates with WooCommerce, OpenCart, and custom APIs.

- **Fees:** 0% (network fees only)
- **Custody:** Non-custodial
- **Focus:** Multi-crypto
- **Deployment:** Docker
- **Stack:** Python, Django
- **License:** GPL-3.0

[Source Code](https://github.com/vsys-host/shkeeper.io) · [Website](https://shkeeper.io) · [Demo](https://shkeeper.io)

---

### DV.Merchant

[![GitHub stars](https://img.shields.io/github/stars/dv-net/dv-merchant?style=flat-square)](https://github.com/dv-net/dv-merchant)

High-performance, self-hosted payments platform built in Go. Supports multi-blockchain acceptance and CEX integrations (Binance, OKX, KuCoin, ByBit, HTX). Fiber v3 HTTP API with Casbin RBAC.

- **Fees:** 0% (network fees only)
- **Custody:** Non-custodial
- **Focus:** Multi-chain + CEX integration
- **Deployment:** Docker, binary
- **Stack:** Go, PostgreSQL, Redis
- **License:** MIT

[Source Code](https://github.com/dv-net/dv-merchant) · [Website](https://dv.net) · [Docs](https://docs.dv.net)

---

### BitcartCC

[![GitHub stars](https://img.shields.io/github/stars/bitcartcc/bitcartcc?style=flat-square)](https://github.com/bitcartcc/bitcartcc)

Open-source cryptocurrency payment processor with a full admin panel. Supports multiple coins and Lightning Network.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Multi-crypto, Lightning
- **Deployment:** Docker
- **Stack:** Python
- **License:** MIT

[Source Code](https://github.com/bitcartcc/bitcartcc) · [Website](https://bitcartcc.com)

---

### ZeroPay

[![GitHub stars](https://img.shields.io/github/stars/ZeroPayDev/ZeroPay?style=flat-square)](https://github.com/ZeroPayDev/ZeroPay)

Lightweight, self-hosted payment gateway for stablecoins and crypto. Built in Rust. Supports x402 Agent-to-Agent payment protocol for AI agents. EVM chains.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Stablecoins, x402, AI agents
- **Deployment:** Docker, binary
- **Stack:** Rust
- **License:** GPL-3.0

[Source Code](https://github.com/ZeroPayDev/ZeroPay) · [Website](https://zpaynow.com)

---

### PayRam

[![GitHub stars](https://img.shields.io/github/stars/PayRam/payram-scripts?style=flat-square)](https://github.com/PayRam/payram-scripts)

Docker-based self-hosted crypto payment gateway with broad OS support (Ubuntu, Debian, CentOS, Fedora, Arch, macOS). AES-256 encryption, Let's Encrypt SSL, guided setup. Headless CLI for AI agents.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Multi-OS, Docker
- **Deployment:** Docker, script
- **Stack:** Shell, Docker
- **License:** MIT

[Source Code](https://github.com/PayRam/payram-scripts) · [Website](https://payram.io)

---

### Keagate

[![GitHub stars](https://img.shields.io/github/stars/dilan-dio4/Keagate?style=flat-square)](https://github.com/dilan-dio4/Keagate)

Self-hosted, high-performance cryptocurrency payment gateway. Funds go directly to your wallet via one-time payment addresses. Includes built-in invoicing client.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Lightweight, API-first
- **Deployment:** Docker, binary
- **Stack:** TypeScript
- **License:** MIT

[Source Code](https://github.com/dilan-dio4/Keagate)

---

### SatSale

[![GitHub stars](https://img.shields.io/github/stars/nickfarrow/SatSale?style=flat-square)](https://github.com/nickfarrow/SatSale)

Lightweight, self-hosted Bitcoin payment processor written in Python. Supports Lightning Network. Minimal resource requirements.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Bitcoin, Lightning
- **Deployment:** Docker, Python
- **Stack:** Python
- **License:** MIT

[Source Code](https://github.com/nickfarrow/SatSale)

---

### ArxMint

[![GitHub stars](https://img.shields.io/github/stars/Traviseric/arxmint?style=flat-square)](https://github.com/Traviseric/arxmint)

Self-hosted Bitcoin payment infrastructure supporting ecash (Cashu), Lightning, and Fedimint federations. Zero-knowledge encrypted backups, managed DNS, auto-HTTPS. Positioned as a "Stripe alternative" for Bitcoin.

- **Fees:** 0% (ecash), ~0.1% (Lightning routing)
- **Custody:** Non-custodial
- **Focus:** Bitcoin, ecash, Lightning, Fedimint
- **Deployment:** Docker Compose
- **Stack:** Next.js, TypeScript, PostgreSQL
- **License:** MIT

[Source Code](https://github.com/Traviseric/arxmint) · [Website](https://arxmint.io)

---

### CryptoPayServer

[![GitHub stars](https://img.shields.io/github/stars/cryptopayserver00/cryptopayserver?style=flat-square)](https://github.com/cryptopayserver00/cryptopayserver)

Open-source crypto payment server for receiving payments across multiple blockchains. Zero telemetry, privacy-first. Modern web UI built with React.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Multi-blockchain, portfolio
- **Deployment:** Docker, binary
- **Stack:** TypeScript, React
- **License:** MIT

[Source Code](https://github.com/cryptopayserver00/cryptopayserver) · [Website](https://cryptopayserver.online)

---

### BTPay

[![GitHub stars](https://img.shields.io/github/stars/btpay-org/btpay?style=flat-square)](https://github.com/btpay-org/btpay)

Lightweight, privacy-focused self-hosted Bitcoin payment processor. Supports on-chain Bitcoin (xpub/output descriptors), BTCPay Server connector, LNbits, stablecoins across 8 chains (Ethereum, Arbitrum, Base, Polygon, Optimism, Avalanche, TRON, Solana), and wire transfers. No database — JSON file persistence.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Bitcoin + stablecoins + fiat
- **Deployment:** Binary
- **Stack:** Python
- **License:** MIT

[Source Code](https://github.com/btpay-org/btpay) · [Website](https://btpay.app)

---

### Sovereign Payment Kernel

[![GitHub stars](https://img.shields.io/github/stars/MEF-works/payment-kernel?style=flat-square)](https://github.com/MEF-works/payment-kernel)

A self-hostable payment operating system that handles Bitcoin, Lightning, Cash App, Venmo, and Zelle from a single kernel. Multi-rail orchestration with ed25519-signed settlement proofs.

- **Fees:** 0%
- **Custody:** Non-custodial
- **Focus:** Multi-rail (crypto + P2P fiat)
- **Deployment:** Docker Compose + installer CLI
- **Stack:** TypeScript, Docker
- **License:** MIT

[Source Code](https://github.com/MEF-works/payment-kernel)

---

## Bitcoin & Lightning Network

Solutions focused specifically on Bitcoin and Lightning Network payment processing.

| Project | Description | Lightning | Stack | License |
|---------|-------------|:---------:|-------|:-------:|
| [LNBits](https://github.com/lnbits/lnbits) | Lightning wallet and accounts system with extensions | ✅ Yes | Python | MIT |
| [LNURL Daemon](https://github.com/nbd-wtf/lnurl-daemon) | LNURL-pay and LNURL-withdraw daemon | ✅ Yes | Go | MIT |
| [LnMe](https://github.com/lnme/lnme) | Simple self-hosted Lightning payment page | ✅ Yes | Node.js | MIT |
| [CypherpunkPay](https://github.com/CypherpunkPay/CypherpunkPay) | Privacy-focused self-hosted Bitcoin processor | ✅ Yes | C# | MIT |

---

## Stablecoin Payment Solutions

Solutions with first-class support for USDT, USDC, and other stablecoins.

| Project | Chains | Stablecoins | Custody | Fees |
|---------|--------|-------------|:-------:|:----:|
| **XPayLabs** | TRON, Ethereum, BSC, Polygon, Arbitrum, Optimism, Base, Avalanche, SUI | USDT, USDC, DAI, BUSD | Non-custodial | 0% |
| **ZeroPay** | EVM chains | USDT, USDC | Non-custodial | 0% |
| **BTPay** | Ethereum, Arbitrum, Base, Polygon, Optimism, Avalanche, TRON, Solana | USDC, USDT, DAI, PYUSD | Non-custodial | 0% |
| **CryptoPayServer** | Multiple chains | USDT, USDC | Non-custodial | 0% |

---

## Payment Orchestration & Multi-Rail

Middleware and orchestration layers that connect multiple payment rails behind a single API.

| Project | Description | Rails | Stack | License |
|---------|-------------|-------|-------|:-------:|
| [Sovereign Payment Kernel](https://github.com/MEF-works/payment-kernel) | OS for payments — routes to best available rail | Bitcoin, Lightning, Cash App, Venmo, Zelle | TypeScript | MIT |
| [toll-booth](https://github.com/willpaul/toll-booth) | HTTP 402 payment middleware for Node.js | Lightning, Cashu, stablecoins | Node.js | MIT |

---

## Libraries & SDKs

First-party SDKs and client libraries for integrating self-hosted crypto payment gateways.

| Project | Language | Gateway | Package |
|---------|----------|---------|---------|
| [XPayLabs Node SDK](https://github.com/neilyan/XPayLabs-node-sdk) | TypeScript | XPayLabs | [npm](https://www.npmjs.com/package/@xpaylabs/node-sdk) |
| [XPayLabs Java SDK](https://github.com/neilyan/XPayLabs-java-sdk) | Java | XPayLabs | [Maven Central](https://central.sonatype.com/artifact/io.xpay/xpay-java-sdk) |
| [BTCPay Server Greenfield API](https://docs.btcpayserver.org/API/Greenfield/v1/) | Any (REST) | BTCPay Server | OpenAPI |
| [BTCPay Server .NET Client](https://github.com/btcpayserver/btcpayserver-dotnet-client) | C# | BTCPay Server | NuGet |
| [BTCPay Server JS Client](https://github.com/btcpayserver/btcpayserver-js-client) | JavaScript | BTCPay Server | npm |
| [BTCPay Server Python Client](https://github.com/btcpayserver/btcpayserver-python-client) | Python | BTCPay Server | PyPI |
| [SHKeeper API](https://shkeeper.io/api) | Any (REST) | SHKeeper | HTTP |

---

## Plugins & CMS Integrations

Plugins that connect self-hosted gateways to popular e-commerce platforms and CMSs.

| Plugin | Platform | Gateway | License |
|--------|----------|---------|:-------:|
| [BTCPay WooCommerce](https://github.com/btcpayserver/woocommerce-plugin) | WooCommerce | BTCPay Server | MIT |
| [BTCPay Shopify](https://github.com/btcpayserver/btcpayserver-shopify-plugin) | Shopify | BTCPay Server | MIT |
| [BTCPay Magento](https://github.com/btcpayserver/magento-plugin) | Magento | BTCPay Server | MIT |
| [SHKeeper WooCommerce](https://github.com/vsys-host/shkeeper.io) | WooCommerce | SHKeeper | GPL-3.0 |
| [SHKeeper OpenCart](https://github.com/vsys-host/shkeeper.io) | OpenCart | SHKeeper | GPL-3.0 |

---

## Utilities & Tools

Supplementary tools for self-hosted crypto payment operations.

| Tool | Description |
|------|-------------|
| [x402 Protocol](https://github.com/x402/x402) | HTTP 402 payment protocol for AI agents and API gateways |
| [Lightning MCP Server](https://github.com/nbd-wtf/lightning-mcp) | MCP server for Lightning Network operations |
| [mempool.space](https://github.com/mempool/mempool) | Self-hosted blockchain explorer and API (Bitcoin, Liquid, Lightning) |
| [Esplora](https://github.com/Blockstream/esplora) | Self-hosted blockchain explorer |

---

## Resources & Guides

### Articles

- [Self-Hosted Crypto Payment Gateways: The Complete Guide](https://xpaylabs.com/blog/self-hosted-crypto-payment-gateways-guide)
- [BTCPay Server vs XPayLabs: Choosing the Right Self-Hosted Payment Processor](https://xpaylabs.com/blog/btcpayserver-vs-xpaylabs)
- [How to Deploy a Self-Hosted Payment Gateway with Docker](https://xpaylabs.com/blog/deploy-self-hosted-payment-gateway-docker)
- [Accept Stablecoin Payments Without Third-Party Fees](https://xpaylabs.com/blog/accept-stablecoin-payments-no-fees)

### Comparisons

- [XPayLabs vs BitPay](https://xpaylabs.com/alternatives/bitpay)
- [XPayLabs vs Coinbase Commerce](https://xpaylabs.com/alternatives/coinbase-commerce)
- [XPayLabs vs NowPayments](https://xpaylabs.com/alternatives/nowpayments)
- [XPayLabs vs OpenNode](https://xpaylabs.com/alternatives/opennode)
- [XPayLabs vs BTCPay Server](https://xpaylabs.com/alternatives/btcpay-server)
- [XPayLabs vs CoinGate](https://xpaylabs.com/alternatives/coingate)

### Communities

- [BTCPay Server Community Chat](https://chat.btcpayserver.org)
- [XPayLabs GitHub Discussions](https://github.com/neilyan/XPayLabs-java/discussions)
- [r/BitcoinMerchants](https://reddit.com/r/BitcoinMerchants)
- [Awesome Self-Hosted](https://github.com/awesome-selfhosted/awesome-selfhosted)

---

## Comparison Table

A high-level comparison of the major self-hosted payment gateways.

| Project | Stablecoins | BTC/LN | Non-Custodial | SDKs | Docker | Min RAM | License |
|---------|:-----------:|:------:|:-------------:|:----:|:------:|:-------:|:-------:|
| **XPayLabs** | ✅ TRON, EVM, SUI | ❌ | ✅ | Java, Node | ✅ | 8 GB | MIT |
| BTCPay Server | ❌ | ✅ BTC, LN, Liquid | ✅ | C#, JS, Python | ✅ | 2 GB | MIT |
| SHKeeper | ✅ ETH-based | ✅ BTC | ✅ | REST | ✅ | 2 GB | GPL-3.0 |
| DV.Merchant | ✅ Multi-chain | ✅ BTC | ✅ | REST | ✅ | 1 GB | MIT |
| BitcartCC | Limited | ✅ BTC, LN | ✅ | REST | ✅ | 1 GB | MIT |
| ZeroPay | ✅ EVM | ❌ | ✅ | REST | ✅ | 512 MB | GPL-3.0 |
| PayRam | ✅ | ✅ | ✅ | CLI | ✅ | 2 GB | MIT |
| Keagate | ❌ | ✅ BTC | ✅ | REST | ✅ | 1 GB | MIT |
| SatSale | ❌ | ✅ BTC, LN | ✅ | REST | ✅ | 256 MB | MIT |
| ArxMint | ❌ | ✅ BTC, LN, ecash | ✅ | REST | ✅ | 4 GB | MIT |
| BTPay | ✅ 8 chains | ✅ BTC via xpub | ✅ | REST | ❌ | 256 MB | MIT |
| Sovereign Kernel | ❌ | ✅ BTC, LN | ✅ | REST | ✅ | 1 GB | MIT |

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

To add a project to this list:
1. The project must be **open-source** (MIT, Apache-2.0, GPL, or similar OSI-approved license)
2. The project must be **self-hostable** on your own infrastructure
3. The project must be actively maintained or in stable/usable state
4. Submit a PR with the project in the appropriate category

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
