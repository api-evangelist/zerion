---
name: Subscribe to real-time wallet activity webhooks
description: Create and manage a Zerion transaction subscription so your server receives real-time JSON:API webhook callbacks when a watched wallet sends or receives a transaction.
api: openapi/zerion-openapi-original.yml
operations:
  - createSubscriptionWalletTransactions
  - GetWalletTransactionsSubscription
  - PatchSubscribedWalletsInSubscription
  - UpdateCallbackUrlInSubscription
  - DisableSubscription
---

# Subscribe to real-time wallet activity webhooks

## Auth
HTTP Basic: `Authorization: Basic <base64("YOUR_API_KEY:")>`.
Base URL `https://api.zerion.io`.

## Steps
1. **Create a subscription** — `createSubscriptionWalletTransactions`
   (`POST /v1/tx-subscriptions/`) with a `callback_url` and a list of wallet
   `addresses`. Optionally scope with `chain_ids`. Free plan allows 5 wallets per
   subscription (paid: unlimited); up to 100 wallets per request.
2. **Add/replace watched wallets later** — `PatchSubscribedWalletsInSubscription`
   (`PATCH /v1/tx-subscriptions/{subscription_id}/wallets`).
3. **Change the callback URL** — `UpdateCallbackUrlInSubscription`
   (`PATCH /v1/tx-subscriptions/{subscription_id}/callback_url`).
4. **Inspect a subscription** — `GetWalletTransactionsSubscription`
   (`GET /v1/tx-subscriptions/{subscription_id}`).
5. **Pause** — `DisableSubscription`
   (`PATCH /v1/tx-subscriptions/{subscription_id}/disable`).

## Receiving callbacks
Zerion POSTs a JSON:API body: `data.type = "callback"` with the transaction in
`included[]`. Verify authenticity every time:
1. Build the signing string `${X-Timestamp}\n${request_body}\n`.
2. Fetch the certificate from the `X-Certificate-URL` header (cache it).
3. Verify `X-Signature` (Base64 RSA-SHA256, PKCS1v15) against the signing string.

## Rules (delivery is best-effort)
- **Be idempotent**: deduplicate on transaction `hash` + `chain`; the same
  notification can arrive more than once and out of order.
- **Handle rollbacks**: a reorg sends a second callback with
  `included[0].attributes.deleted == true` — remove/mark that tx.
- Return `200` fast and process async. `5xx`/timeout is retried up to 3 times
  (~20s apart); a `4xx` is treated as acknowledged and not retried.
- Prices are always `null` in callbacks — fetch separately via the Fungibles API.
- Callback URLs must be whitelisted via the dashboard for production.
