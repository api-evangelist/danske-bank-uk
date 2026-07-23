---
name: Initiate a domestic payment (PIS)
description: >-
  Create a domestic payment consent, confirm funds, and execute a single
  immediate domestic payment through Danske Bank (UK)'s UK Open Banking PIS API.
api: openapi/danske-bank-uk-payment-initiation-openapi.json
operations:
  - CreateDomesticPaymentConsents
  - GetDomesticPaymentConsentsConsentId
  - GetDomesticPaymentConsentsConsentIdFundsConfirmation
  - CreateDomesticPayments
  - GetDomesticPaymentsDomesticPaymentId
---

# Initiate a domestic payment (PIS)

Move a single immediate domestic (Faster Payments) payment as an FCA-authorised
PISP under UK Open Banking Read/Write PIS v4.0. This is a `physical`/`write`
consequence action — treat it as money movement.

## Prerequisites
- PISP onboarding via the Open Banking Directory; FAPI OAuth2/OIDC + mutual TLS.
- Base URL: `https://obp-api.danskebank.com/open-banking/v4.0/pisp`

## Required headers (see conventions/danske-bank-uk-conventions.yml)
- `Authorization: Bearer <token>`
- `x-idempotency-key` — unique per payment instruction; guarantees at-most-once
  processing. **Always send this on POSTs.**
- `x-jws-signature` — detached JWS over the request body.
- `x-fapi-interaction-id`, `x-fapi-auth-date`, `x-fapi-customer-ip-address`.

## Steps
1. **Create the payment consent** — `CreateDomesticPaymentConsents` with a
   client-credentials token (scope `payments`): the debtor (optional), creditor
   account, `InstructedAmount`, and remittance information. Capture `ConsentId`.
2. **Authorize** — redirect the PSU through OAuth2/OIDC authorization-code with SCA,
   binding the `ConsentId`; obtain a PSU access token.
3. **Confirm funds** (optional) — `GetDomesticPaymentConsentsConsentIdFundsConfirmation`.
4. **Verify consent status** — `GetDomesticPaymentConsentsConsentId` should be
   `Authorised`.
5. **Execute the payment** — `CreateDomesticPayments` referencing the `ConsentId`,
   with a fresh `x-idempotency-key`. The `Initiation` block MUST match the consent
   exactly or the bank rejects it.
6. **Poll status** — `GetDomesticPaymentsDomesticPaymentId` until the status
   reaches a terminal value (e.g. `AcceptedSettlementCompleted`).

## Error handling
On a duplicate `x-idempotency-key` with a differing body you get a `409`. Field
validation failures return `400` with `OBError1` items pin-pointing the JSON
`Path`. Never retry a payment without reusing the same idempotency key. See
errors/danske-bank-uk-problem-types.yml.
