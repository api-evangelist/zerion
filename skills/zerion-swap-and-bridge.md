---
name: Get swap and bridge quotes
description: Retrieve quotes for same-chain swaps and cross-chain bridges between two fungible assets (EVM chains and Solana, including EVM<->Solana) using the Zerion API.
api: openapi/zerion-openapi-original.yml
operations:
  - swapFungibles
  - swapQuotes
---

# Get swap and bridge quotes

## Auth
HTTP Basic: `Authorization: Basic <base64("YOUR_API_KEY:")>`.
Base URL `https://api.zerion.io`.

## Steps
1. **(Cross-chain only) List bridgeable tokens** — `swapFungibles`
   (`GET /v1/swap/fungibles/`). Populates a token picker for a given
   input/output chain pair. Same-chain swaps skip this step.
2. **Get quotes** — `swapQuotes` (`GET /v1/swap/quotes/`). Returns quotes from
   multiple liquidity sources for a same-chain swap or a cross-chain bridge
   between two fungible assets. Supports EVM chains and Solana, including
   EVM <-> Solana bridges.

## Rules
- The API returns quotes/ready-to-sign transaction data; signing and broadcast
  happen in your own wallet stack (or via the Zerion CLI's `swap`/`bridge`).
- JSON:API responses; check the error `errors[]` envelope on non-2xx.
- Retry only `429`/`500` with exponential backoff.
