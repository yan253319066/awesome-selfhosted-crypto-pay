
<p align="center">
  <img src="https://raw.githubusercontent.com/yan253319066/awesome-selfhosted-crypto-pay/main/assets/logo.svg" width="200" alt="Awesome Self-Hosted Crypto Pay">
</p>

<h1 align="center">Awesome Self-Hosted Crypto Pay <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a></h1>

<p align="center">
  <a href="README.md">English</a> | <strong>中文</strong>
</p>

<p align="center">
  <strong>自托管加密货币支付网关精选清单</strong> —— 在你自己的服务器上运行的开源加密支付软件，无需第三方费用或托管。
</p>

> 精选的 **自托管加密货币支付网关、处理器和基础设施**清单 —— 在你自己的服务器上运行的开源软件，无需第三方费用或托管私钥。

自托管加密支付网关意味着 **没有月费、没有交易抽成、不需要 KYC、完全掌控你的私钥。** 客户的付款直接进入你的钱包。

本清单涵盖 Bitcoin/Lightning 方案、稳定币处理器、多支付轨道编排层以及介于两者之间的所有内容。

---

## 目录

- [精选推荐](#精选推荐)
- [全栈支付网关](#全栈支付网关)
- [Bitcoin 和 Lightning Network](#bitcoin--lightning-network)
- [稳定币支付方案](#稳定币支付方案)
- [支付编排和多支付轨道](#支付编排和多支付轨道)
- [库和 SDK](#库和-sdk)
- [插件和 CMS 集成](#插件和-cms-集成)
- [工具和实用程序](#工具和实用程序)
- [资源与指南](#资源与指南)
- [对比表](#对比表)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

---

## 精选推荐

### XPayLabs

[![GitHub stars](https://img.shields.io/github/stars/yan253319066/XPayLabs-docker?style=flat-square)](https://github.com/yan253319066/XPayLabs-docker)
[![GitHub license](https://img.shields.io/github/license/yan253319066/XPayLabs-docker?style=flat-square)](https://github.com/yan253319066/XPayLabs-docker/blob/main/LICENSE)

**XPayLabs (xpay)** —— 自托管加密支付基础设施。零网关费用。非托管稳定币支付网关，支持 TRON（TRC-20）、EVM 链（Ethereum、BSC、Polygon、Arbitrum、Optimism、Base、Avalanche）和 SUI。现已支持 **x402 Agent-to-Agent 支付协议**，适用于 AI 代理和自治系统。

- **零费率** —— 0% 网关费用，仅需区块链 Gas 费（TRON 约 $0.01）
- **非托管** —— 私钥在你的 Docker 容器中生成和存储
- **多链支持** —— TRON、Ethereum、BSC、Polygon、Arbitrum、Optimism、Base、Avalanche、SUI
- **x402 协议** —— AI 代理的 Agent-to-Agent 支付
- **白标结账** —— 完全可定制，无第三方品牌
- **实时交易检测** —— 亚秒级交易扫描
- **开发者 API** —— Stripe 风格的 REST API，HMAC-SHA256 签名 Webhook
- **官方 SDK** —— Node.js/TypeScript（`@xpaylabs/node-sdk`）、Java/Spring Boot（`xpay-java-sdk`）和 REST API
- **部署** —— `docker compose up -d`，一键部署
- **价格** —— 免费（自托管），可选付费支持计划

[源代码](https://github.com/yan253319066/XPayLabs-docker) · [网站](https://xpaylabs.com) · [文档](https://docs.xpaylabs.com) · [演示](https://github.com/neilyan/XPayLabs-demo-vue) · [Node SDK](https://github.com/neilyan/XPayLabs-node-sdk) · [Java SDK](https://github.com/neilyan/XPayLabs-java-sdk)

---

## 全栈支付网关

可以在你自己的基础设施上部署的、完整的、生产就绪的支付网关。

### BTCPay Server

[![GitHub stars](https://img.shields.io/github/stars/btcpayserver/btcpayserver?style=flat-square)](https://github.com/btcpayserver/btcpayserver)

最成熟的自托管 Bitcoin 支付处理器。支持链上 Bitcoin、Lightning Network（LND、CLN、Eclair）和 Liquid。多租户、发票、POS 应用、众筹和捐赠页面。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** Bitcoin、Lightning、Liquid
- **部署方式：** Docker、手动
- **技术栈：** C#、.NET
- **许可证：** MIT

[源代码](https://github.com/btcpayserver/btcpayserver) · [网站](https://btcpayserver.org) · [文档](https://docs.btcpayserver.org)

---

### SHKeeper

[![GitHub stars](https://img.shields.io/github/stars/vsys-host/shkeeper.io?style=flat-square)](https://github.com/vsys-host/shkeeper.io)

支持 Bitcoin、Ethereum、USDT 和其他代币的自托管加密货币支付网关。集成 WooCommerce、OpenCart 和自定义 API。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 多币种
- **部署方式：** Docker
- **技术栈：** Python、Django
- **许可证：** GPL-3.0

[源代码](https://github.com/vsys-host/shkeeper.io) · [网站](https://shkeeper.io)

---

### DV.Merchant

[![GitHub stars](https://img.shields.io/github/stars/dv-net/dv-merchant?style=flat-square)](https://github.com/dv-net/dv-merchant)

用 Go 编写的高性能自托管支付平台。支持多链收款和 CEX 集成（Binance、OKX、KuCoin、ByBit、HTX）。提供 Fiber v3 HTTP API 和 Casbin RBAC。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 多链 + CEX 集成
- **部署方式：** Docker、二进制
- **技术栈：** Go、PostgreSQL、Redis
- **许可证：** MIT

[源代码](https://github.com/dv-net/dv-merchant) · [网站](https://dv.net) · [文档](https://docs.dv.net)

---



### ZeroPay

[![GitHub stars](https://img.shields.io/github/stars/ZeroPayDev/ZeroPay?style=flat-square)](https://github.com/ZeroPayDev/ZeroPay)

轻量级自托管稳定币和加密货币支付网关。用 Rust 构建。支持 AI 代理的 x402 Agent-to-Agent 支付协议。兼容 EVM 链。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 稳定币、x402、AI 代理
- **部署方式：** Docker、二进制
- **技术栈：** Rust
- **许可证：** GPL-3.0

[源代码](https://github.com/ZeroPayDev/ZeroPay) · [网站](https://zpaynow.com)

---

### PayRam

[![GitHub stars](https://img.shields.io/github/stars/PayRam/payram-scripts?style=flat-square)](https://github.com/PayRam/payram-scripts)

基于 Docker 的自托管加密支付网关，支持多种操作系统（Ubuntu、Debian、CentOS、Fedora、Arch、macOS）。AES-256 加密、Let's Encrypt SSL、引导式安装。支持 AI 代理的无头命令行接口。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 多系统、Docker
- **部署方式：** Docker、脚本
- **技术栈：** Shell、Docker
- **许可证：** MIT

[源代码](https://github.com/PayRam/payram-scripts) · [网站](https://payram.io)

---

### Keagate

[![GitHub stars](https://img.shields.io/github/stars/dilan-dio4/Keagate?style=flat-square)](https://github.com/dilan-dio4/Keagate)

自托管的高性能加密货币支付网关。通过一次性支付地址将资金直接转入你的钱包。包含内置发票客户端。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 轻量级、API 优先
- **部署方式：** Docker、二进制
- **技术栈：** TypeScript
- **许可证：** MIT

[源代码](https://github.com/dilan-dio4/Keagate)

---

### SatSale

[![GitHub stars](https://img.shields.io/github/stars/nickfarrow/SatSale?style=flat-square)](https://github.com/nickfarrow/SatSale)

用 Python 编写的轻量级自托管 Bitcoin 支付处理器。支持 Lightning Network。资源需求极低。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** Bitcoin、Lightning
- **部署方式：** Docker、Python
- **技术栈：** Python
- **许可证：** MIT

[源代码](https://github.com/nickfarrow/SatSale)

---

### ArxMint

[![GitHub stars](https://img.shields.io/github/stars/Traviseric/arxmint?style=flat-square)](https://github.com/Traviseric/arxmint)

自托管 Bitcoin 支付基础设施，支持 ecash（Cashu）、Lightning 和 Fedimint 联邦。零知识加密备份、托管 DNS、自动 HTTPS。定位为 Bitcoin 领域的"Stripe 替代品"。

- **费用：** 0%（ecash），约 0.1%（Lightning 路由）
- **托管方式：** 非托管
- **专注领域：** Bitcoin、ecash、Lightning、Fedimint
- **部署方式：** Docker Compose
- **技术栈：** Next.js、TypeScript、PostgreSQL
- **许可证：** MIT

[源代码](https://github.com/Traviseric/arxmint) · [网站](https://arxmint.io)

---

### CryptoPayServer

[![GitHub stars](https://img.shields.io/github/stars/cryptopayserver00/cryptopayserver?style=flat-square)](https://github.com/cryptopayserver00/cryptopayserver)

开源加密支付服务器，支持在多个区块链上接收付款。零遥测、隐私优先。使用 React 构建的现代化 Web 界面。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 多链、投资组合
- **部署方式：** Docker、二进制
- **技术栈：** TypeScript、React
- **许可证：** MIT

[源代码](https://github.com/cryptopayserver00/cryptopayserver) · [网站](https://cryptopayserver.online)

---

### BTPay

[![GitHub stars](https://img.shields.io/github/stars/btpay-org/btpay?style=flat-square)](https://github.com/btpay-org/btpay)

轻量级、注重隐私的自托管 Bitcoin 支付处理器。支持链上 Bitcoin（xpub/output descriptors）、BTCPay Server 连接器、LNbits、跨 8 条链的稳定币（Ethereum、Arbitrum、Base、Polygon、Optimism、Avalanche、TRON、Solana）以及银行转账。无需数据库 —— 使用 JSON 文件持久化。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** Bitcoin + 稳定币 + 法币
- **部署方式：** 二进制
- **技术栈：** Python
- **许可证：** MIT

[源代码](https://github.com/btpay-org/btpay) · [网站](https://btpay.app)

---

### Sovereign Payment Kernel

[![GitHub stars](https://img.shields.io/github/stars/MEF-works/payment-kernel?style=flat-square)](https://github.com/MEF-works/payment-kernel)

一个可自托管的支付操作系统，从单个内核处理 Bitcoin、Lightning、Cash App、Venmo 和 Zelle。多轨道编排，带 ed25519 签名的结算证明。

- **费用：** 0%
- **托管方式：** 非托管
- **专注领域：** 多轨道（加密货币 + P2P 法币）
- **部署方式：** Docker Compose + 安装 CLI
- **技术栈：** TypeScript、Docker
- **许可证：** MIT

[源代码](https://github.com/MEF-works/payment-kernel)

---

## Bitcoin & Lightning Network

专注于 Bitcoin 和 Lightning Network 支付处理的方案。

| 项目 | 描述 | Lightning | 技术栈 | 许可证 |
|---------|-------------|:---------:|-------|:-------:|
| [LNBits](https://github.com/lnbits/lnbits) | 带扩展功能的 Lightning 钱包和账户系统 | ✅ 是 | Python | MIT |
| [LNURL Daemon](https://github.com/nbd-wtf/lnurl-daemon) | LNURL-pay 和 LNURL-withdraw 守护进程 | ✅ 是 | Go | MIT |
| [LnMe](https://github.com/bumi/lnme) | 简单的自托管 Lightning 支付页面 | ✅ 是 | Node.js | MIT |
| [CypherpunkPay](https://github.com/CypherpunkPay/CypherpunkPay) | 注重隐私的自托管 Bitcoin 处理器 | ✅ 是 | C# | MIT |

---

## 稳定币支付方案

优先支持 USDT、USDC 和其他稳定币的方案。

| 项目 | 支持的链 | 稳定币 | 托管方式 | 费率 |
|---------|--------|-------------|:-------:|:----:|
| **XPayLabs** | TRON、Ethereum、BSC、Polygon、Arbitrum、Optimism、Base、Avalanche、SUI | USDT、USDC、DAI、BUSD | 非托管 | 0% |
| **ZeroPay** | EVM 链 | USDT、USDC | 非托管 | 0% |
| **BTPay** | Ethereum、Arbitrum、Base、Polygon、Optimism、Avalanche、TRON、Solana | USDC、USDT、DAI、PYUSD | 非托管 | 0% |
| **CryptoPayServer** | 多条链 | USDT、USDC | 非托管 | 0% |

---

## 支付编排和多支付轨道

在单一 API 后面连接多个支付轨道的中间件和编排层。

| 项目 | 描述 | 支持的支付轨道 | 技术栈 | 许可证 |
|---------|-------------|-------|-------|:-------:|
| [Sovereign Payment Kernel](https://github.com/MEF-works/payment-kernel) | 支付操作系统 —— 路由到最优可用轨道 | Bitcoin、Lightning、Cash App、Venmo、Zelle | TypeScript | MIT |
| [toll-booth](https://github.com/forgesworn/toll-booth) | 支付轨道无关的 L402 API 中间件。Lightning、Cashu、x402 | Lightning、Cashu、稳定币 | TypeScript | MIT |

---

## 库和 SDK

用于集成自托管加密支付网关的官方 SDK 和客户端库。

| 项目 | 语言 | 网关 | 包地址 |
|---------|----------|---------|---------|
| [XPayLabs Node SDK](https://github.com/neilyan/XPayLabs-node-sdk) | TypeScript | XPayLabs | [npm](https://www.npmjs.com/package/@xpaylabs/node-sdk) |
| [XPayLabs Java SDK](https://github.com/neilyan/XPayLabs-java-sdk) | Java | XPayLabs | [Maven Central](https://central.sonatype.com/artifact/io.xpay/xpay-java-sdk) |
| [XPayLabs REST API](https://docs.xpaylabs.com) | 任意（REST） | XPayLabs | [文档](https://docs.xpaylabs.com/api-reference/overview) |
| [BTCPay Server Greenfield API](https://docs.btcpayserver.org/API/Greenfield/v1/) | 任意（REST） | BTCPay Server | OpenAPI |
| [BTCPay Server .NET Client](https://github.com/btcpayserver/btcpayserver-dotnet-client) | C# | BTCPay Server | NuGet |
| [BTCPay Server JS Client](https://github.com/btcpayserver/btcpayserver-js-client) | JavaScript | BTCPay Server | npm |
| [BTCPay Server Python Client](https://github.com/btcpayserver/btcpayserver-python-client) | Python | BTCPay Server | PyPI |
| [SHKeeper API](https://shkeeper.io/api) | 任意（REST） | SHKeeper | HTTP |

---

## 插件和 CMS 集成

将自托管支付网关连接到流行电商平台和 CMS 的插件。

| 插件 | 平台 | 网关 | 许可证 |
|--------|----------|---------|:-------:|
| [BTCPay WooCommerce](https://github.com/btcpayserver/woocommerce-plugin) | WooCommerce | BTCPay Server | MIT |
| [BTCPay Shopify](https://github.com/btcpayserver/btcpayserver-shopify-plugin) | Shopify | BTCPay Server | MIT |
| [BTCPay Magento](https://github.com/btcpayserver/magento-plugin) | Magento | BTCPay Server | MIT |
| [SHKeeper WooCommerce](https://github.com/vsys-host/shkeeper.io) | WooCommerce | SHKeeper | GPL-3.0 |
| [SHKeeper OpenCart](https://github.com/vsys-host/shkeeper.io) | OpenCart | SHKeeper | GPL-3.0 |

---

## 工具和实用程序

自托管加密支付运营的辅助工具。

| 工具 | 描述 |
|------|-------------|
| [x402 Protocol](https://github.com/x402/x402) | 用于 AI 代理和 API 网关的 HTTP 402 支付协议 |
| [Lightning MCP Server](https://github.com/nbd-wtf/lightning-mcp) | Lightning Network 操作的 MCP 服务器 |
| [mempool.space](https://github.com/mempool/mempool) | 自托管区块链浏览器和 API（Bitcoin、Liquid、Lightning） |
| [Esplora](https://github.com/Blockstream/esplora) | 自托管区块链浏览器 |

---

## 资源与指南

### 文章

- [自托管加密支付网关完全指南](https://xpaylabs.com/zh/blog/self-hosted-crypto-payment-gateways-guide)
- [BTCPay Server vs XPayLabs：选择合适的自托管支付处理器](https://xpaylabs.com/zh/blog/btcpayserver-vs-xpaylabs)
- [如何用 Docker 部署自托管支付网关](https://xpaylabs.com/zh/blog/deploy-self-hosted-payment-gateway-docker)
- [无需第三方费用即可接受稳定币支付](https://xpaylabs.com/zh/blog/accept-stablecoin-payments-no-fees)

### 对比

- [XPayLabs vs BitPay](https://xpaylabs.com/zh/alternatives/bitpay)
- [XPayLabs vs Coinbase Commerce](https://xpaylabs.com/zh/alternatives/coinbase-commerce)
- [XPayLabs vs NowPayments](https://xpaylabs.com/zh/alternatives/nowpayments)
- [XPayLabs vs OpenNode](https://xpaylabs.com/zh/alternatives/opennode)
- [XPayLabs vs BTCPay Server](https://xpaylabs.com/zh/alternatives/btcpay-server)
- [XPayLabs vs CoinGate](https://xpaylabs.com/zh/alternatives/coingate)

### 社区

- [BTCPay Server 社区聊天](https://chat.btcpayserver.org)
- [XPayLabs GitHub 讨论区](https://github.com/yan253319066/XPayLabs-docker/discussions)
- [r/BitcoinMerchants](https://reddit.com/r/BitcoinMerchants)
- [Awesome Self-Hosted](https://github.com/awesome-selfhosted/awesome-selfhosted)

---

## 对比表

主要自托管支付网关的高级对比。

| 项目 | 稳定币 | BTC/LN | 非托管 | SDK | Docker | 最低内存 | 许可证 |
|---------|:-----------:|:------:|:-------------:|:----:|:------:|:-------:|:-------:|
| **XPayLabs** | ✅ TRON、EVM、SUI | ❌ | ✅ | Java、Node、REST | ✅ | 8 GB | MIT |
| BTCPay Server | ❌ | ✅ BTC、LN、Liquid | ✅ | C#、JS、Python | ✅ | 2 GB | MIT |
| SHKeeper | ✅ 基于 ETH | ✅ BTC | ✅ | REST | ✅ | 2 GB | GPL-3.0 |
| DV.Merchant | ✅ 多链 | ✅ BTC | ✅ | REST | ✅ | 1 GB | MIT |
| ZeroPay | ✅ EVM | ❌ | ✅ | REST | ✅ | 512 MB | GPL-3.0 |
| PayRam | ✅ | ✅ | ✅ | CLI | ✅ | 2 GB | MIT |
| Keagate | ❌ | ✅ BTC | ✅ | REST | ✅ | 1 GB | MIT |
| SatSale | ❌ | ✅ BTC、LN | ✅ | REST | ✅ | 256 MB | MIT |
| ArxMint | ❌ | ✅ BTC、LN、ecash | ✅ | REST | ✅ | 4 GB | MIT |
| BTPay | ✅ 8 条链 | ✅ BTC via xpub | ✅ | REST | ❌ | 256 MB | MIT |
| Sovereign Kernel | ❌ | ✅ BTC、LN | ✅ | REST | ✅ | 1 GB | MIT |

---

## 贡献指南

欢迎贡献！请先阅读[贡献指南](CONTRIBUTING.md)。

向此列表添加项目的要求：
1. 项目必须是**开源**的（MIT、Apache-2.0、GPL 或类似的 OSI 批准许可证）
2. 项目必须可**自托管**在你自己的基础设施上
3. 项目必须处于活跃维护或稳定/可用状态
4. 提交 PR 将项目添加到相应的分类中

---

## 许可证

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

在法律允许的范围内，贡献者已放弃该作品的所有版权及相关或邻接权利。
