---
name: Retrieve account information (AIS)
description: >-
  Set up an account-access consent and read a customer's accounts, balances and
  transactions from Danske Bank (UK) via the UK Open Banking AIS API.
api: openapi/danske-bank-uk-account-transaction-openapi.json
operations:
  - CreateAccountAccessConsents
  - GetAccountAccessConsentsConsentId
  - GetAccounts
  - GetAccountsAccountId
  - GetAccountsAccountIdBalances
  - GetAccountsAccountIdTransactions
---

# Retrieve account information (AIS)

Read a payment service user's (PSU) account, balance and transaction data from
Danske Bank (UK) under the UK Open Banking Read/Write AIS v4.0 API. You must be
an FCA-authorised (or agent) AISP onboarded via the Open Banking Directory.

## Prerequisites
- TPP onboarding complete; eIDAS/OBIE transport and signing certificates in place.
- A FAPI-compliant OAuth2/OIDC client. Transport uses mutual TLS.
- Base URL: `https://obp-api.danskebank.com/open-banking/v4.0/aisp`

## Required headers (see conventions/danske-bank-uk-conventions.yml)
- `Authorization: Bearer <token>`
- `x-fapi-interaction-id` (client UUID, echoed back for tracing)
- `x-fapi-auth-date`, `x-fapi-customer-ip-address` where applicable

## Steps
1. **Create the consent** — `CreateAccountAccessConsents` with a client-credentials
   token, specifying the `Permissions` you need (e.g. ReadAccountsDetail,
   ReadBalances, ReadTransactionsDetail) and an ExpirationDateTime. Capture the
   returned `ConsentId`.
2. **Authorize** — redirect the PSU through OAuth2/OIDC authorization-code with SCA,
   binding the `ConsentId`; exchange the code for a PSU access token (scope `accounts`).
3. **Verify consent** (optional) — `GetAccountAccessConsentsConsentId` to confirm
   status is `Authorised`.
4. **List accounts** — `GetAccounts` to enumerate the consented accounts and their
   `AccountId`s.
5. **Read balances** — `GetAccountsAccountIdBalances` for a given `AccountId`.
6. **Read transactions** — `GetAccountsAccountIdTransactions`; follow `Links.Next`
   for pagination and use `fromBookingDateTime`/`toBookingDateTime` filters.

## Error handling
Failures return the OBIE `OBErrorResponse1` envelope (`Errors[]` with ErrorCode,
Message, Path). A `403` with an invalid-consent-status code means the consent
expired or was revoked — recreate and re-authorize. See
errors/danske-bank-uk-problem-types.yml.
