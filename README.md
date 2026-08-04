# Tensor (tensor)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
