# Triton One (triton-one)

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

Triton One is a high-performance Solana RPC and blockchain infrastructure provider operating globally distributed bare-metal node networks for Solana, Pythnet, Sui, and Monad. Beyond standard Solana JSON-RPC, Triton ships the Yellowstone ecosystem — Dragon's Mouth gRPC streaming, Whirligig WebSockets, Fumarole persistent streams, Old Faithful historical archive, Steamboat custom indexes, Vixen program parsing, Jet QUIC transaction sending, and Shield transaction policies — plus the hosted Metaplex Digital Assets API, Cascade SWQoS transaction delivery, and trading APIs (Pyth Hermes, Jito bundles, Metis, Titan). The Customers REST API at customers.triton.one programmatically manages accounts, subscriptions, endpoints, tokens, address watch lists, and rate tiers. Pricing is a single unified pay-as-you-go model with a $125 prepaid deposit and no tier gating.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/triton-one/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/triton-one/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Solana
- RPC
- Blockchain
- Web3
- Streaming
- Yellowstone
- Validator
- gRPC
- Pythnet
- Sui
- Monad

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Triton One Customers API

REST API for managing Triton One customer accounts, subscriptions (Developer, Mainnet-Shared, Mainnet-Dedicated), RPC endpoints, RPC consumption tokens, address watch lists, and rate tiers. Token-based authentication via the Authorization header; tokens scope to reseller, operator, or read-only roles. Hosted at customers.triton.one/api/v1.

- **Human URL:** [https://docs.triton.one/account-management/api-access/introduction](https://docs.triton.one/account-management/api-access/introduction)
- **Base URL:** `https://customers.triton.one/api/v1`

#### Tags

- Solana
- RPC
- Account Management
- Customers

#### Properties

- [Documentation](https://docs.triton.one/account-management/api-access/introduction)
- [Authentication](https://docs.triton.one/account-management/api-access/auth-and-headers)
- [Documentation](https://docs.triton.one/account-management/api-access/accounts)
- [Documentation](https://docs.triton.one/account-management/api-access/subscriptions)
- [Documentation](https://docs.triton.one/account-management/api-access/endpoints)
- [Documentation](https://docs.triton.one/account-management/api-access/tokens)
- [Documentation](https://docs.triton.one/account-management/api-access/address-watch-lists)
- [Documentation](https://docs.triton.one/account-management/api-access/rate-tiers)
- [Documentation](https://docs.triton.one/account-management/api-access/subscription-types)
- [OpenAPI](openapi/triton-one-customers-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/triton-one-account-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/triton-one-subscription-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/triton-one-endpoint-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/triton-one-token-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/triton-one-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Triton One Solana RPC API

Triton's enhanced Solana JSON-RPC interface. Exposes the full Solana JSON-RPC surface plus Triton's custom extensions — getTransactionsForAddress (single-call address history with slot, blockTime, status, and tokenAccounts filters and pagination) and the percentile-aware getRecentPrioritizationFees. Backed by global bare-metal nodes with GeoDNS routing.

- **Human URL:** [https://docs.triton.one/chains/solana](https://docs.triton.one/chains/solana)
- **Base URL:** `https://${endpoint}.rpcpool.com`

#### Tags

- Solana
- RPC
- JSON-RPC
- Priority Fees
- Streaming

#### Properties

- [Documentation](https://docs.triton.one/chains/solana)
- [Documentation](https://docs.triton.one/chains/solana/improved-priority-fees-api)
- [Documentation](https://docs.triton.one/chains/solana/gettransactionsforaddress)
- [Documentation](https://docs.triton.one/chains/solana/streaming)
- [Documentation](https://docs.triton.one/chains/solana/geyser)
- [Documentation](https://docs.triton.one/chains/solana/cascade)
- [Documentation](https://docs.triton.one/chains/solana/token-program)
- [OpenAPI](openapi/triton-one-solana-rpc-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Digital Assets API

Hosted Metaplex Digital Assets Standard (DAS) implementation served from the same Triton RPC endpoint. Read methods for compressed and standard NFTs (getAsset, getAssets, getAssetProof(s), getAssetSignatures, searchAssets, getAssetsBy{Owner,Creator,Authority}, getNftEditions) plus SPL token introspection (getTokenAccounts, getTokenLargestAccounts). Powered by Triton's Photon indexer.

- **Human URL:** [https://docs.triton.one/digital-assets-api/introduction](https://docs.triton.one/digital-assets-api/introduction)
- **Base URL:** `https://${endpoint}.rpcpool.com`

#### Tags

- Solana
- Digital Assets
- Metaplex
- NFT
- DAS

#### Properties

- [Documentation](https://docs.triton.one/digital-assets-api/introduction)
- [Documentation](https://docs.triton.one/digital-assets-api/metaplex-digital-assets-api)
- [Documentation](https://docs.triton.one/digital-assets-api/fungible-assets)
- [OpenAPI](openapi/triton-one-digital-assets-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Yellowstone gRPC (Dragon's Mouth)

Dragon's Mouth — Triton's high-performance Solana streaming gRPC service. Subscribe to slots, blocks, transactions, accounts, and blockmeta updates over a single bidirectional gRPC stream. Open-source server reference at github.com/rpcpool/yellowstone-grpc (Rust, AGPL-3.0).

- **Human URL:** [https://docs.triton.one/project-yellowstone/dragons-mouth-grpc-subscriptions](https://docs.triton.one/project-yellowstone/dragons-mouth-grpc-subscriptions)

#### Tags

- Solana
- gRPC
- Streaming
- Yellowstone

#### Properties

- [Documentation](https://docs.triton.one/project-yellowstone/introduction)
- [Documentation](https://docs.triton.one/project-yellowstone/dragons-mouth-grpc-subscriptions)
- [Source Code](https://github.com/rpcpool/yellowstone-grpc)
- [SDK](https://github.com/rpcpool/yellowstone-grpc)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Fumarole Persistent Streams

Fumarole — persistent Yellowstone streams with gap-free reconnect and 4-day server-side cache. Built for consumers that must not miss events across client restarts or network blips.

- **Human URL:** [https://docs.triton.one/project-yellowstone/fumarole](https://docs.triton.one/project-yellowstone/fumarole)

#### Tags

- Solana
- Streaming
- Yellowstone
- Fumarole

#### Properties

- [Documentation](https://docs.triton.one/project-yellowstone/fumarole)
- [Source Code](https://github.com/rpcpool/yellowstone-fumarole)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Whirligig WebSockets

Whirligig — Triton's enhanced WebSocket layer over Solana RPC. Adds the missing transactionSubscribe stream and hardened account/slot subscribe behaviour with stable backpressure.

- **Human URL:** [https://docs.triton.one/project-yellowstone/whirligig-websockets](https://docs.triton.one/project-yellowstone/whirligig-websockets)

#### Tags

- Solana
- WebSocket
- Streaming
- Yellowstone

#### Properties

- [Documentation](https://docs.triton.one/project-yellowstone/whirligig-websockets)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Old Faithful Historical Archive

Old Faithful — content-addressable, queryable archive of all Solana history from genesis. Complete-ledger queries in milliseconds, flat-rate pricing across all epochs and methods. Open-source server at github.com/rpcpool/yellowstone-faithful (Go, AGPL-3.0).

- **Human URL:** [https://docs.triton.one/project-yellowstone/old-faithful-historical-archive](https://docs.triton.one/project-yellowstone/old-faithful-historical-archive)

#### Tags

- Solana
- Archive
- Historical Data
- Yellowstone

#### Properties

- [Documentation](https://docs.triton.one/project-yellowstone/old-faithful-historical-archive)
- [Documentation](https://docs.triton.one/chains/solana/old-faithful-historical-archive-1)
- [Source Code](https://github.com/rpcpool/yellowstone-faithful)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Cascade Transaction Delivery

Cascade — high-performance transaction delivery network leveraging Solana's Stake-Weighted Quality of Service (SWQoS). Routes transactions through reserved, private connection pools of staked validators instead of congested public ports. Integrates with Yellowstone Shield for on-chain transaction policies. Open-source sender at github.com/rpcpool/yellowstone-jet.

- **Human URL:** [https://docs.triton.one/chains/solana/cascade](https://docs.triton.one/chains/solana/cascade)

#### Tags

- Solana
- Transactions
- SWQoS
- Cascade

#### Properties

- [Documentation](https://docs.triton.one/chains/solana/cascade)
- [Documentation](https://docs.triton.one/chains/solana/cascade/sending-txs)
- [Documentation](https://docs.triton.one/chains/solana/cascade/buying-transaction-bandwidth)
- [Documentation](https://docs.triton.one/chains/solana/cascade/providing-transaction-bandwidth)
- [Source Code](https://github.com/rpcpool/yellowstone-jet)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Triton One Trading APIs

Hosted trading APIs available on the Triton platform — Pyth Hermes price feeds, Jito bundle simulation, Metis Swap, and Titan Swap. Metered separately under the unified PAYG pricing model.

- **Human URL:** [https://docs.triton.one/trading-apis/introduction](https://docs.triton.one/trading-apis/introduction)

#### Tags

- Solana
- Trading
- Swap
- Pyth
- Jito

#### Properties

- [Documentation](https://docs.triton.one/trading-apis/introduction)
- [Documentation](https://docs.triton.one/trading-apis/hermes)
- [Documentation](https://docs.triton.one/trading-apis/bundle-simulation-with-jito)
- [Documentation](https://docs.triton.one/trading-apis/metis-swap-api)
- [Documentation](https://docs.triton.one/trading-apis/titan-swap-api)
- [Postman Collection](collections/triton-one-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-digital-assets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-digital-assets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/triton-one-solana-rpc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/triton-one-solana-rpc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://triton.one)
- [Documentation](https://docs.triton.one)
- [Pricing](https://triton.one/pricing)
- [Status Page](https://status.triton.one)
- [GitHub Organization](https://github.com/rpcpool)
- [LinkedIn](https://www.linkedin.com/company/triton-one)
- [Twitter](https://twitter.com/triton_one)
- [Support](mailto:support@triton.one)
- [Getting Started](https://docs.triton.one/getting-started)
- [Terms of Service](https://triton.one/terms)
- [Privacy Policy](https://docs.triton.one/core-features/privacy-and-security)
- [Rate Limits](https://docs.triton.one/core-features/ratelimits)
- [Authentication](https://docs.triton.one/account-management/api-access/auth-and-headers)
- [Tiers](https://docs.triton.one/account-management/api-access/rate-tiers)
- [SDK](https://github.com/rpcpool/yellowstone-grpc)
- [SDK](https://github.com/rpcpool/yellowstone-vixen)
- [SDK](https://github.com/rpcpool/yellowstone-jet)
- [SDK](https://github.com/rpcpool/yellowstone-fumarole)
- [SDK](https://github.com/rpcpool/yellowstone-faithful)
- [Tools](https://github.com/rpcpool/solana-rpc-ansible)
- [Plans](https://plans/triton-one-plans-pricing.yml)
- [Rate Limits](https://rate-limits/triton-one-rate-limits.yml)
- [Fin Ops](https://finops/triton-one-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
