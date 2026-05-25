# Triton One (triton-one)
Triton One is a high-performance Solana RPC and blockchain infrastructure provider operating globally distributed bare-metal node networks for Solana, Pythnet, Sui, and Monad. Beyond standard Solana JSON-RPC, Triton ships the Yellowstone ecosystem — Dragon's Mouth gRPC streaming, Whirligig WebSockets, Fumarole persistent streams, Old Faithful historical archive, Steamboat custom indexes, Vixen program parsing, Jet QUIC transaction sending, and Shield transaction policies — plus the hosted Metaplex Digital Assets API, Cascade SWQoS transaction delivery, and trading APIs (Pyth Hermes, Jito bundles, Metis, Titan). The Customers REST API at customers.triton.one programmatically manages accounts, subscriptions, endpoints, tokens, address watch lists, and rate tiers. Pricing is a single unified pay-as-you-go model with a $125 prepaid deposit and no tier gating.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/triton-one/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Solana, RPC, Blockchain, Web3, Streaming, Yellowstone, Validator, gRPC, Pythnet, Sui, Monad

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Supported Chains

| Chain | Notes |
|---|---|
| Solana | Primary focus; mainnet-beta, testnet, devnet |
| Pythnet | 1,700+ price feeds |
| Sui | Includes Walrus storage docs |
| Monad | EVM-compatible L1 |

## Subscription Types

| Type | Description |
|---|---|
| `developer` | Devnet + testnet endpoints, typically free |
| `mainnet-shared` | Mainnet shared pool |
| `mainnet-dedicated` | Reserved bare-metal capacity with isolated streaming |

## Rate Tiers

`free`, `tier1`, `tier2`, `tier3`, `dedi` — RPS and concurrency caps configured per endpoint.

## APIs

### Triton One Customers API
REST API at `customers.triton.one/api/v1` for managing accounts, subscriptions, RPC endpoints, RPC consumption tokens, address watch lists, and rate tiers. Bearer token authentication; tokens scope to reseller, operator, or read-only roles.

**Human URL:** [https://docs.triton.one/account-management/api-access/introduction](https://docs.triton.one/account-management/api-access/introduction)

- [Documentation — Introduction](https://docs.triton.one/account-management/api-access/introduction)
- [Documentation — Auth & Headers](https://docs.triton.one/account-management/api-access/auth-and-headers)
- [OpenAPI](openapi/triton-one-customers-api-openapi.yml)
- [JSON Schema — Account](json-schema/triton-one-account-schema.json)
- [JSON Schema — Subscription](json-schema/triton-one-subscription-schema.json)
- [JSON Schema — Endpoint](json-schema/triton-one-endpoint-schema.json)
- [JSON Schema — Token](json-schema/triton-one-token-schema.json)
- [JSON-LD](json-ld/triton-one-context.jsonld)
- [Naftiko Capability — Accounts](capabilities/customers-accounts.yaml)
- [Naftiko Capability — Subscriptions](capabilities/customers-subscriptions.yaml)
- [Naftiko Capability — Endpoints](capabilities/customers-endpoints.yaml)
- [Naftiko Capability — Tokens](capabilities/customers-tokens.yaml)
- [Naftiko Capability — Address Watch Lists](capabilities/customers-address-watch-lists.yaml)

### Triton One Solana RPC API
Triton's enhanced Solana JSON-RPC interface. Full Solana JSON-RPC surface plus Triton custom extensions: `getTransactionsForAddress` (single-call consolidated address history with slot, blockTime, status, and tokenAccounts filters and pagination) and the percentile-aware `getRecentPrioritizationFees`.

**Human URL:** [https://docs.triton.one/chains/solana](https://docs.triton.one/chains/solana)

- [Documentation — Solana](https://docs.triton.one/chains/solana)
- [Documentation — Improved Priority Fees](https://docs.triton.one/chains/solana/improved-priority-fees-api)
- [Documentation — getTransactionsForAddress](https://docs.triton.one/chains/solana/gettransactionsforaddress)
- [OpenAPI](openapi/triton-one-solana-rpc-api-openapi.yml)
- [Naftiko Capability — Solana RPC](capabilities/solana-rpc.yaml)

### Triton One Digital Assets API
Hosted Metaplex Digital Assets Standard (DAS) at the same RPC endpoint. Read methods for compressed and standard NFTs and SPL token introspection. Powered by Triton's Photon indexer.

**Human URL:** [https://docs.triton.one/digital-assets-api/introduction](https://docs.triton.one/digital-assets-api/introduction)

- [Documentation — DAS](https://docs.triton.one/digital-assets-api/metaplex-digital-assets-api)
- [OpenAPI](openapi/triton-one-digital-assets-api-openapi.yml)
- [Naftiko Capability — Digital Assets RPC](capabilities/digital-assets-rpc.yaml)

### Triton One Yellowstone gRPC (Dragon's Mouth)
High-performance Solana streaming over gRPC. Subscribe to slots, blocks, transactions, accounts, and blockmeta updates over a single bidirectional stream.

**Human URL:** [https://docs.triton.one/project-yellowstone/dragons-mouth-grpc-subscriptions](https://docs.triton.one/project-yellowstone/dragons-mouth-grpc-subscriptions)

- [Source — yellowstone-grpc](https://github.com/rpcpool/yellowstone-grpc)

### Triton One Fumarole Persistent Streams
Persistent Yellowstone streams with gap-free reconnect and 4-day server-side cache.

- [Documentation](https://docs.triton.one/project-yellowstone/fumarole)
- [Source — yellowstone-fumarole](https://github.com/rpcpool/yellowstone-fumarole)

### Triton One Whirligig WebSockets
Enhanced WebSocket layer over Solana RPC. Adds the missing `transactionSubscribe` stream.

- [Documentation](https://docs.triton.one/project-yellowstone/whirligig-websockets)

### Triton One Old Faithful Historical Archive
Content-addressable, queryable archive of all Solana history from genesis. Complete-ledger queries in milliseconds; flat-rate pricing across all epochs.

- [Documentation](https://docs.triton.one/project-yellowstone/old-faithful-historical-archive)
- [Source — yellowstone-faithful](https://github.com/rpcpool/yellowstone-faithful)

### Triton One Cascade Transaction Delivery
SWQoS-based transaction delivery routing through reserved private connection pools of staked validators. Integrates with Yellowstone Shield for on-chain transaction policies.

- [Documentation](https://docs.triton.one/chains/solana/cascade)
- [Source — yellowstone-jet](https://github.com/rpcpool/yellowstone-jet)

### Triton One Trading APIs
Pyth Hermes price feeds, Jito bundle simulation, Metis Swap, Titan Swap, Titan Prime.

- [Documentation](https://docs.triton.one/trading-apis/introduction)

## Open Source — `github.com/rpcpool`

| Repo | Language | Description |
|---|---|---|
| `yellowstone-grpc` | Rust | Dragon's Mouth gRPC service (AGPL-3.0) |
| `yellowstone-faithful` | Go | Old Faithful archive (AGPL-3.0) |
| `yellowstone-vixen` | Rust | Solana program parsing toolkit (MIT) |
| `yellowstone-jet` | Rust | QUIC tx sender with proxy + SwQoS (AGPL-3.0) |
| `yellowstone-fumarole` | Rust | Persistent stream component (AGPL-3.0) |
| `solana-rpc-ansible` | Shell | Ansible playbooks for Solana RPC nodes |
| `solana-cluster` | Go | Tooling to manage Solana snapshots (Apache-2.0) |
| `digital-asset-rpc-infrastructure` | Rust | DAS infrastructure (AGPL-3.0) |
| `photon` | Rust | Indexer powering the Metaplex DAS endpoint (Apache-2.0) |

## Pricing

Triton One uses a single unified **pay-as-you-go** model — no tiers, no feature gating, no overage premiums.

- **Minimum prepaid deposit:** $125 USD (non-refundable, 12-month validity)
- **Standard RPC, indexed accounts, ledger queries:** $0.08/GB bandwidth + $10/million calls
- **Streaming services, Titan Prime API:** $0.08/GB bandwidth
- **Metaplex DAS / Photon:** $0.08/GB bandwidth + $50/million calls
- **Metis API:** $0.08/GB bandwidth + $80/million calls

Every Triton product is included on every account. See [`plans/triton-one-plans-pricing.yml`](plans/triton-one-plans-pricing.yml) for the API Commons Plans 0.1 representation.

## Rate Limits

Rate limits are tier-driven (`free`, `tier1`, `tier2`, `tier3`, `dedi`) and configured per endpoint. See [`rate-limits/triton-one-rate-limits.yml`](rate-limits/triton-one-rate-limits.yml).

## FinOps

See [`finops/triton-one-finops.yml`](finops/triton-one-finops.yml) for the FOCUS-aligned billing surface.

## Maintainers

- Kin Lane — [API Evangelist](https://apievangelist.com)
