---
name: Fetch and interpret wallet transaction history
description: Retrieve a wallet's decoded transaction history with human-readable operation types and transfer details using the Zerion API.
api: openapi/zerion-openapi-original.yml
operations:
  - listWalletTransactions
---

# Fetch and interpret wallet transaction history

## Auth
HTTP Basic: `Authorization: Basic <base64("YOUR_API_KEY:")>`.
Base URL `https://api.zerion.io`.

## Steps
1. Call `listWalletTransactions`
   (`GET /v1/wallets/{address}/transactions/`).
2. Narrow results with filters:
   - `filter[operation_types]` (e.g. `send,receive,trade,execute`)
   - `filter[chain_ids]` (e.g. `ethereum,base`)
   - `filter[min_mined_at]` — a 13-digit millisecond timestamp (exactly 13 digits, or you get a `400`)
   - `filter[trash]` to include/exclude spam
3. Page through with `page[size]` (max 100) and follow `links.next`.

## Interpreting a transaction
- `attributes.operation_type` — `send`, `receive`, `trade`, `execute`, etc.
- `attributes.status` — `confirmed` or `failed`.
- `attributes.transfers[]` — token movements with `direction`, `quantity`, `fungible_info`.
- `attributes.application_metadata` — present only for recognized contract
  interactions (carries dapp `name`, `contract_address`, `method`).
- `relationships.chain.id` — the chain the tx occurred on.

## Rules
- JSON:API responses; empty `data[]` (200) means no matches, not an error.
- Validate the 13-digit millisecond format before sending to avoid `400`.
- Retry only `429`/`500` with exponential backoff.
