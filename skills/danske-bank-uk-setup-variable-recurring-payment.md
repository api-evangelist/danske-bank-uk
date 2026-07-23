---
name: Set up a variable recurring payment (VRP)
description: >-
  Establish a domestic VRP consent and execute recurring payments within agreed
  control parameters using Danske Bank (UK)'s UK Open Banking VRP API.
api: openapi/danske-bank-uk-variable-recurring-payments-openapi.json
operations:
  - domesticVrpConsentsPost
  - domesticVrpConsentsGet
  - domesticVrpConsentsFundsConfirmation
  - domesticVrpPost
  - domesticVrpGet
---

# Set up a variable recurring payment (VRP)

Establish a long-lived domestic VRP consent then execute individual payments
within the PSU-agreed limits, under UK Open Banking Read/Write VRP v4.0.

## Prerequisites
- PISP onboarding via the Open Banking Directory; FAPI OAuth2/OIDC + mutual TLS.
- Base URL: `https://obp-api.danskebank.com/open-banking/v4.0/pisp`

## Required headers (see conventions/danske-bank-uk-conventions.yml)
- `Authorization: Bearer <token>`, `x-idempotency-key` (on POSTs),
  `x-jws-signature`, and the `x-fapi-*` set.

## Steps
1. **Create the VRP consent** — `domesticVrpConsentsPost` defining the
   `ControlParameters` (maximum individual amount, periodic limits, valid-from/to)
   and creditor. Capture the consent id.
2. **Authorize** — PSU authorization-code + SCA binds the consent; obtain the PSU token.
3. **Verify consent** — `domesticVrpConsentsGet` to confirm `Authorised` status.
4. **Confirm funds** (optional) — `domesticVrpConsentsFundsConfirmation` before a run.
5. **Execute a recurring payment** — `domesticVrpPost` referencing the consent, with
   a fresh `x-idempotency-key`; the instructed amount must fall inside the
   `ControlParameters`.
6. **Check status** — `domesticVrpGet` to read the executed VRP payment status.

## Error handling
Breaching a control parameter (amount or period limit) returns a `400`/`403` with
the relevant `OBError1` code. Idempotency and validation rules are identical to
the single-payment flow. See errors/danske-bank-uk-problem-types.yml.
