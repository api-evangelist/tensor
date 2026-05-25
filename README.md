# Tensor (tensor)

Tensor is the Solana-native NFT marketplace and trading protocol founded by Tensor HQ and now stewarded by the Tensor Foundation. The platform exposes a public read REST API, a transaction-construction (TX) API that returns unsigned Solana transactions for list / buy / bid / pool flows, and a WebSocket subscription stream for realtime marketplace events. Five open-source Anchor programs — Marketplace, AMM v2, Whitelist, Escrow, and Fees — back the protocol and ship as `@tensor-foundation/*` JavaScript SDKs and `tensor-*` Rust crates. Tensor supports legacy NFTs, programmable NFTs (pNFT), and Bubblegum compressed NFTs (cNFT), and serves as the execution layer behind aggregators, wallets, sales bots, and AMM bonding-curve liquidity providers across the Solana ecosystem. Governance and ecosystem grants flow through the TNSR token and the Tensor DAO on Realms.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/tensor/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

NFT, Marketplace, Solana, Blockchain, Web3, Cryptocurrency, Trading, DAO, DeFi, AMM

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## TNSR Token

| Field | Value |
|---|---|
| Mint | `TNSRxcUxoT9xBG3de7PiJyTDYu7kskLqcpddxnEJAS6` |
| Total supply | 1,000,000,000 |
| Distribution | 55% community, 27% core contributors, 9% investors and advisors, 9% future fundraising / development |
| Vesting | Core / investors: 3-year linear with 1-year cliff. Half of community treasury: 3-year linear, no cliff. |
| DAO | https://app.realms.today/dao/TNSR |
| Steward | Tensor Foundation |

## APIs

### Tensor API
Read-only REST surface covering collections, NFT mint metadata, active listings, bids (collection / single-NFT / trait), TSwap and TAmm pool state, user portfolios, transaction history, royalty enforcement metadata, priority fee oracle, and whitelist verification. Authentication via the `x-tensor-api-key` header.

**Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)

- [Documentation](https://dev.tensor.trade/reference)
- [Authentication](https://dev.tensor.trade/docs/authentication)
- [OpenAPI](openapi/tensor-api-openapi.yml)
- [JSON Schema — Collection](json-schema/tensor-collection-schema.json)
- [JSON Schema — Listing](json-schema/tensor-listing-schema.json)
- [JSON Schema — Bid](json-schema/tensor-bid-schema.json)
- [JSON Schema — Mint](json-schema/tensor-mint-schema.json)
- [JSON Schema — Pool](json-schema/tensor-pool-schema.json)
- [JSON-LD](json-ld/tensor-context.jsonld)
- [Naftiko Capability — Marketplace Read](capabilities/marketplace-read.yaml)
- [Example — Find Collection](examples/tensor-collection-find-example.json)
- [Example — Active Listings](examples/tensor-active-listings-example.json)

### Tensor Transaction (TX) API
Server-side transaction construction that returns base64-encoded unsigned Solana transactions for list / delist / edit-listing / buy / place-collection-bid / place-single-nft-bid / place-trait-bid / accept-bid / cancel-bid / pool create-edit-close / pool deposit-withdraw / escrow deposit-withdraw. Supports legacy NFTs, pNFTs, and cNFTs; clients sign locally with the user's wallet and submit.

**Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)

- [OpenAPI](openapi/tensor-tx-api-openapi.yml)
- [Naftiko Capability — Marketplace Trading](capabilities/marketplace-trading.yaml)
- [Example — List](examples/tensor-tx-list-example.json)
- [Example — Buy](examples/tensor-tx-buy-example.json)

### Tensor WebSocket API
Subscription-based realtime stream. Channels: `newTransaction`, `ammOrderUpdate`, `ammOrderUpdateAll`, `tcompBidUpdate`, `tcompBidUpdateAll`, `ping`, `unsubscribe`. Powers floor-price feeds, sales bots, and order-book mirroring.

**Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)

- [AsyncAPI](asyncapi/tensor-websocket-api-asyncapi.yml)
- [Naftiko Capability — Marketplace Streaming](capabilities/marketplace-streaming.yaml)

## On-Chain Programs

| Program | Repo | npm | crates.io |
|---|---|---|---|
| Marketplace | [tensor-foundation/marketplace](https://github.com/tensor-foundation/marketplace) | [`@tensor-foundation/marketplace`](https://www.npmjs.com/package/@tensor-foundation/marketplace) | [`tensor-marketplace`](https://crates.io/crates/tensor-marketplace) |
| AMM v2 | [tensor-foundation/amm](https://github.com/tensor-foundation/amm) | [`@tensor-foundation/amm`](https://www.npmjs.com/package/@tensor-foundation/amm) | [`tensor-amm`](https://crates.io/crates/tensor-amm) |
| Whitelist | [tensor-foundation/whitelist](https://github.com/tensor-foundation/whitelist) | [`@tensor-foundation/whitelist`](https://www.npmjs.com/package/@tensor-foundation/whitelist) | [`tensor-whitelist`](https://crates.io/crates/tensor-whitelist) |
| Escrow | [tensor-foundation/escrow](https://github.com/tensor-foundation/escrow) | [`@tensor-foundation/escrow`](https://www.npmjs.com/package/@tensor-foundation/escrow) | [`tensor-escrow`](https://crates.io/crates/tensor-escrow) |
| Fees | [tensor-foundation/fees](https://github.com/tensor-foundation/fees) | — | — |

## Common Properties

- [Portal — tensor.trade](https://tensor.trade)
- [Portal — Tensor Foundation](https://www.tensor.foundation)
- [Portal — Tensor Developer Hub](https://dev.tensor.trade)
- [Documentation — Developer Hub](https://dev.tensor.trade/docs)
- [Documentation — API Reference](https://dev.tensor.trade/reference)
- [Documentation — Marketplace Help Center](https://docs.tensor.trade/)
- [Documentation — Foundation Docs](https://docs.tensor.foundation/)
- [GettingStarted](https://dev.tensor.trade/docs/getting-started)
- [Authentication](https://dev.tensor.trade/docs/authentication)
- [SignUp — API Access Request](https://airtable.com/apppFpk6Ul9yiI6sw/pagCBazYyAewboZnT/form)
- [GitHubOrganization — Tensor Foundation](https://github.com/tensor-foundation)
- [GitHubOrganization — Tensor HQ](https://github.com/tensor-hq)
- [CodeExamples — SDK Examples](https://github.com/tensor-foundation/SDK-examples)
- [CodeExamples — Next.js Marketplace Template](https://github.com/tensor-hq/marketplace-nextjs-template)
- [CodeExamples — Discord Sales Bot Template](https://github.com/tensor-hq/salesbot-discord-template)
- [CodeExamples — Telegram Floor Checker Template](https://github.com/tensor-hq/fpchecker-telegram-template)
- [Tool — smart-rpc](https://github.com/tensor-hq/smart-rpc)
- [Tool — Unified Wallet Kit](https://github.com/tensor-hq/Unified-Wallet-Kit)
- [Tool — Solana JS toolkit](https://github.com/tensor-hq/toolkit)
- [Tool — Solana Rust toolbox](https://github.com/tensor-hq/toolbox)
- [SocialMedia — Tensor on X](https://twitter.com/tensor_hq)
- [SocialMedia — Tensor DAO on X](https://twitter.com/TNSR_DAO)
- [Forum — Tensor DAO on Realms](https://app.realms.today/dao/TNSR)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Tensor API](openapi/tensor-api-openapi.yml)
- [Tensor Transaction (TX) API](openapi/tensor-tx-api-openapi.yml)

### AsyncAPI

- [Tensor WebSocket API](asyncapi/tensor-websocket-api-asyncapi.yml)

### JSON Schema

- [Tensor Collection](json-schema/tensor-collection-schema.json)
- [Tensor Listing](json-schema/tensor-listing-schema.json)
- [Tensor Bid](json-schema/tensor-bid-schema.json)
- [Tensor Mint](json-schema/tensor-mint-schema.json)
- [Tensor Pool](json-schema/tensor-pool-schema.json)

### JSON-LD

- [Tensor Context](json-ld/tensor-context.jsonld)

### Capabilities (Naftiko)

- [Marketplace — Read](capabilities/marketplace-read.yaml)
- [Marketplace — Trading](capabilities/marketplace-trading.yaml)
- [Marketplace — Realtime Streaming](capabilities/marketplace-streaming.yaml)

### Vocabulary

- [Tensor Vocabulary](vocabulary/tensor-vocabulary.yml)

### Spectral Rules

- [Tensor Rules](rules/tensor-rules.yml)

### Examples

- [Find Collection](examples/tensor-collection-find-example.json)
- [Active Listings](examples/tensor-active-listings-example.json)
- [TX — List NFT](examples/tensor-tx-list-example.json)
- [TX — Buy NFT](examples/tensor-tx-buy-example.json)

### Commercial artifacts

- [Plans / Pricing](plans/tensor-plans-pricing.yml)
- [Rate Limits](rate-limits/tensor-rate-limits.yml)
- [FinOps Definition](finops/tensor-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
