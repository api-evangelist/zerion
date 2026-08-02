---
name: Read a wallet portfolio and PnL
description: Fetch a wallet's total portfolio value, token/DeFi positions, and profit-and-loss across EVM chains and Solana using the Zerion API.
api: openapi/zerion-openapi-original.yml
operations:
  - getWalletPortfolio
  - listWalletPositions
  - getWalletPNL
---

# Read a wallet portfolio and PnL

Use the Zerion API to summarize what a wallet holds and how it has performed.

## Auth
HTTP Basic. Your API key is the username, password is empty: send
`Authorization: Basic <base64("YOUR_API_KEY:")>` (note the trailing colon).
Base URL: `https://api.zerion.io`. Agents without a key can pay per request with
`--x402` (Base/Solana) or `--mpp` (Tempo).

## Steps
1. **Portfolio overview** — call `getWalletPortfolio`
   (`GET /v1/wallets/{address}/portfolio`). Returns total value and breakdown by
   position type and chain. Pass `currency` (default `usd`) if you need another.
2. **List positions** — call `listWalletPositions`
   (`GET /v1/wallets/{address}/positions/`). Filter with `filter[chain_ids]`,
   `filter[position_types]`, or `filter[trash]=only_non_trash` to hide spam.
   Paginate by following `links.next` until absent (`page[size]` max 100).
3. **Profit and loss** — call `getWalletPNL`
   (`GET /v1/wallets/{address}/pnl`). Returns realized, unrealized, net-invested,
   and fee figures (FIFO cost basis).

## Rules
- Responses are JSON:API: read `data`, follow `links.next` for more pages.
- Prices in positions are live; do not cache portfolio value long.
- On `429`, back off using `RateLimit-Org-Second-Reset`; retry `429`/`500` only,
  never `400`/`401` (see errors/zerion-problem-types.yml).
- Spam tokens are labeled `flags.is_trash`; filter them out client-side.
