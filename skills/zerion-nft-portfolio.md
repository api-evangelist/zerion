---
name: Read a wallet NFT portfolio
description: Fetch a wallet's NFT holdings, positions, and collections with metadata and floor prices across supported chains using the Zerion API.
api: openapi/zerion-openapi-original.yml
operations:
  - getWalletNftPortfolio
  - listWalletNFTPositions
  - listWalletNFTCollections
---

# Read a wallet NFT portfolio

## Auth
HTTP Basic: `Authorization: Basic <base64("YOUR_API_KEY:")>`.
Base URL `https://api.zerion.io`.

## Steps
1. **NFT portfolio overview** — `getWalletNftPortfolio`
   (`GET /v1/wallets/{address}/nft-portfolio`). Totals and value of a wallet's
   NFT holdings.
2. **NFT positions** — `listWalletNFTPositions`
   (`GET /v1/wallets/{address}/nft-positions/`). Individual NFTs with metadata
   and media. `page[size]` supports up to 500 on NFT endpoints.
3. **Group by collection** — `listWalletNFTCollections`
   (`GET /v1/wallets/{address}/nft-collections/`). Collections held, with floor
   prices and per-chain breakdown.

## Rules
- JSON:API responses; follow `links.next` to page.
- Filter by `filter[chain_ids]` to scope to specific chains.
- Retry only `429`/`500` with exponential backoff.
