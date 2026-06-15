# Tensor (tensor)

Tensor is the Solana-native NFT marketplace and trading protocol founded by Tensor HQ and now stewarded by the Tensor Foundation. The platform exposes a public read REST API, a transaction-construction (TX) API that returns unsigned Solana transactions for list / buy / bid / pool flows, and a WebSocket subscription stream for realtime marketplace events. Five open-source Anchor programs — Marketplace, AMM v2, Whitelist, Escrow, and Fees — back the protocol and ship as `@tensor-foundation/*` JavaScript SDKs and `tensor-*` Rust crates. Tensor supports legacy NFTs, programmable NFTs (pNFT), and Bubblegum compressed NFTs (cNFT), and serves as the execution layer behind aggregators, wallets, sales bots, and AMM bonding-curve liquidity providers across the Solana ecosystem. Governance and ecosystem grants flow through the TNSR token and the Tensor DAO on Realms.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tensor/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tensor/refs/heads/main/apis.yml)

## Scope

- **Type:** APIs.json
- **Position:** Providing

## Tags

- NFT
- Marketplace
- Solana
- Blockchain
- Web3
- Cryptocurrency
- Trading
- DAO
- DeFi
- AMM

## Timestamps

- **Created:** 2026-05-24T00:00:00.000Z
- **Modified:** 2026-05-24

## APIs

### Tensor API

Read API surface for the Tensor marketplace covering collections, NFT mint metadata, active listings, bids (collection-wide, single-NFT, trait), TSwap and TAmm pool state, user portfolios, transaction history, royalty enforcement metadata, priority fee oracle, and whitelist verification. Authenticate via the `x-tensor-api-key` header issued through the Tensor Developer Hub.

- **Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)
- **Base URL:** `https://api.mainnet.tensordev.io`

#### Tags

- NFT
- Marketplace
- Solana
- Blockchain
- Web3
- Trading
- Collections
- Listings
- Bids
- Read

#### Properties

- [Documentation](https://dev.tensor.trade/reference)
- [Documentation](https://dev.tensor.trade/docs/authentication)
- [OpenAPI](openapi/tensor-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tensor-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tensor-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/tensor-collection-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tensor-listing-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tensor-bid-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tensor-mint-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tensor-pool-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/tensor-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Examples](examples/tensor-collection-find-example.json)
- [Examples](examples/tensor-active-listings-example.json)

### Tensor Transaction API

Server-side transaction construction API that returns base64-encoded unsigned Solana transactions for the canonical Tensor marketplace flows — list, delist, edit listing, buy, place/accept/cancel collection bid, single-NFT bid, trait bid, deposit/withdraw escrow, create/edit/close AMM pool. Clients sign locally with the user's wallet and submit. Covers standard NFTs, programmable NFTs (pNFT), and compressed NFTs (cNFT).

- **Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)
- **Base URL:** `https://api.mainnet.tensordev.io`

#### Tags

- NFT
- Marketplace
- Solana
- Blockchain
- Web3
- Trading
- Transactions
- Listings
- Bids
- Write

#### Properties

- [Documentation](https://dev.tensor.trade/reference)
- [OpenAPI](openapi/tensor-tx-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tensor-tx-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tensor-tx-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Examples](examples/tensor-tx-list-example.json)
- [Examples](examples/tensor-tx-buy-example.json)

### Tensor WebSocket API

Subscription-based realtime stream of Tensor marketplace events. Channels include `newTransaction` (every confirmed marketplace action), `ammOrderUpdate` / `ammOrderUpdateAll` (TSwap and TAmm pool state), `tcompBidUpdate` / `tcompBidUpdateAll` (compressed-NFT collection bids), `ping`, and `unsubscribe`. Used to power floor-price feeds, sales bots, and order-book mirroring.

- **Human URL:** [https://dev.tensor.trade/reference](https://dev.tensor.trade/reference)
- **Base URL:** `wss://api.mainnet.tensordev.io`

#### Tags

- NFT
- Marketplace
- Solana
- Blockchain
- Web3
- Realtime
- Streaming
- WebSocket
- Events

#### Properties

- [Documentation](https://dev.tensor.trade/reference)
- [AsyncAPI](asyncapi/tensor-websocket-api-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/tensor-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tensor-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/tensor-tx-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tensor-tx-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://tensor.trade)
- [Portal](https://www.tensor.foundation)
- [Portal](https://dev.tensor.trade)
- [Documentation](https://dev.tensor.trade/docs)
- [Documentation](https://dev.tensor.trade/reference)
- [Documentation](https://dev.tensor.trade/changelog)
- [Code Examples](https://dev.tensor.trade/recipes)
- [Getting Started](https://dev.tensor.trade/docs/getting-started)
- [Documentation](https://dev.tensor.trade/docs/authentication)
- [Documentation](https://dev.tensor.trade/docs/sdks-and-examples)
- [Documentation](https://docs.tensor.trade/)
- [Documentation](https://docs.tensor.foundation/)
- [Documentation](https://docs.tensor.foundation/tokenomics)
- [Documentation](https://docs.tensor.foundation/governance)
- [Documentation](https://docs.tensor.foundation/audits)
- [Documentation](https://docs.tensor.foundation/grants)
- [Forum](https://app.realms.today/dao/TNSR)
- [GitHub Organization](https://github.com/tensor-foundation)
- [GitHub Organization](https://github.com/tensor-hq)
- [Source Code](https://github.com/tensor-foundation/marketplace)
- [Source Code](https://github.com/tensor-foundation/amm)
- [Source Code](https://github.com/tensor-foundation/escrow)
- [Source Code](https://github.com/tensor-foundation/whitelist)
- [Source Code](https://github.com/tensor-foundation/fees)
- [SDK](https://www.npmjs.com/package/@tensor-foundation/marketplace)
- [SDK](https://www.npmjs.com/package/@tensor-foundation/amm)
- [SDK](https://www.npmjs.com/package/@tensor-foundation/whitelist)
- [SDK](https://www.npmjs.com/package/@tensor-foundation/escrow)
- [SDK](https://crates.io/crates/tensor-marketplace)
- [SDK](https://crates.io/crates/tensor-amm)
- [SDK](https://crates.io/crates/tensor-whitelist)
- [SDK](https://crates.io/crates/tensor-escrow)
- [SDK](https://www.npmjs.com/package/@tensor-oss/tensorswap-sdk)
- [SDK](https://www.npmjs.com/package/@tensor-oss/tcomp-sdk)
- [SDK](https://www.npmjs.com/package/@tensor-oss/ledger-solana-sdk)
- [Code Examples](https://github.com/tensor-foundation/SDK-examples)
- [Code Examples](https://github.com/tensor-hq/marketplace-nextjs-template)
- [Code Examples](https://github.com/tensor-hq/salesbot-discord-template)
- [Code Examples](https://github.com/tensor-hq/fpchecker-telegram-template)
- [Tool](https://github.com/tensor-hq/toolbox)
- [Tool](https://github.com/tensor-hq/toolkit)
- [Tool](https://github.com/tensor-hq/smart-rpc)
- [Tool](https://github.com/tensor-hq/Unified-Wallet-Kit)
- [Tool](https://github.com/tensor-hq/simple-nft-wash-trade-detection)
- [Sign Up](https://airtable.com/apppFpk6Ul9yiI6sw/pagCBazYyAewboZnT/form)
- [Social Media](https://twitter.com/tensor_hq)
- [Social Media](https://twitter.com/TNSR_DAO)
- [Plans](plans/tensor-plans-pricing.yml)
- [Rate Limits](rate-limits/tensor-rate-limits.yml)
- [Fin Ops](finops/tensor-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
