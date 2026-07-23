# Danske Bank (UK) (danske-bank-uk)

Danske Bank (UK) is the trading name of Northern Bank Limited, a retail and commercial bank headquartered in Belfast and the largest bank in Northern Ireland. It is a wholly owned subsidiary of Denmark's Danske Bank Group, authorised by the UK Prudential Regulation Authority and regulated by the Financial Conduct Authority and PRA. As "Northern Bank Limited t/a Danske Bank" it is one of the CMA9 - the nine largest current-account providers mandated by the UK Competition and Markets Authority to implement the Open Banking standard - and an FCA-authorised ASPSP under PSD2.

It publishes the UK Open Banking (OBIE) API family: a public, unauthenticated Open Data API and the FAPI-secured Read/Write APIs for Account and Transaction Information (AIS), Payment Initiation (PIS), Confirmation of Funds (CBPII), Variable Recurring Payments (VRP), and Events, alongside a suite of premium corporate APIs (account transaction and balance reporting, payment collection, corporate payment initiation, and FX trade reporting and execution) exposed through the Danske Bank developer portal.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/danske-bank-uk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/danske-bank-uk/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- CMA9
- United Kingdom
- Northern Ireland
- Payments
- Account Information
- FAPI
- Fintech

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### Danske Bank (UK) Open Data API

Public, unauthenticated UK Open Banking Open Data API (OBIE Open Data v2.2) publishing reference data for Danske Bank (UK) - ATM and branch locations, personal and business current accounts, unsecured SME loans, and commercial credit cards. Confirmed live (HTTP 200).

- **Human URL:** [https://developers.danskebank.com/api_products/danske_bank_apis/od?view=reference](https://developers.danskebank.com/api_products/danske_bank_apis/od?view=reference)
- **Base URL:** `https://obp-data.danskebank.com/v2.2`

#### Tags

- Open Data
- ATMs
- Branches
- Products
- Public

#### Properties

- [OpenAPI](openapi/danske-bank-uk-opendata-openapi.json)
- [Documentation](https://developers.danskebank.com/api_products/danske_bank_apis/od?view=reference)
- [API Reference](https://developers.danskebank.com/api_products/danske_bank_apis/od?view=reference)

### Danske Bank (UK) Account and Transaction API

OBIE Read/Write Account and Transaction Information API (AIS, v4.0) for account details, balances, transactions, beneficiaries, standing orders, direct debits, and statements. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://obp-api.danskebank.com/open-banking/v4.0/aisp`

#### Tags

- Account Information
- AIS
- Open Banking

#### Properties

- [OpenAPI](openapi/danske-bank-uk-account-transaction-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Payment Initiation API

OBIE Read/Write Payment Initiation API (PIS, v4.0) for domestic, scheduled, standing-order, file, and international payments. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://obp-api.danskebank.com/open-banking/v4.0/pisp`

#### Tags

- Payment Initiation
- PIS
- Payments
- Open Banking

#### Properties

- [OpenAPI](openapi/danske-bank-uk-payment-initiation-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Confirmation of Funds API

OBIE Read/Write Confirmation of Funds API (CBPII, v4.0) for card-based payment instrument issuers to confirm funds availability. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://obp-api.danskebank.com/open-banking/v4.0/cbpii`

#### Tags

- Confirmation of Funds
- CBPII
- Open Banking

#### Properties

- [OpenAPI](openapi/danske-bank-uk-confirmation-of-funds-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Variable Recurring Payments API

OBIE Read/Write Variable Recurring Payments API (VRP, v4.0) for domestic VRP consents and recurring payments within agreed parameters. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://obp-api.danskebank.com/open-banking/v4.0/pisp`

#### Tags

- Variable Recurring Payments
- VRP
- Payments
- Open Banking

#### Properties

- [OpenAPI](openapi/danske-bank-uk-variable-recurring-payments-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Events API

OBIE Read/Write Event Notification API (v4.0) delivering real-time notifications on account and payment activities to registered TPPs. FAPI-secured with OAuth2/OIDC and mutual-TLS.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://obp-api.danskebank.com/open-banking/v4.0`

#### Tags

- Events
- Notifications
- Open Banking

#### Properties

- [OpenAPI](openapi/danske-bank-uk-events-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Account Transaction & Balance API

Premium first-party corporate API providing real-time access to account transactions and balances, with a public mock sandbox.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://api.danskebank.com/corporate/api/v1/account-transaction-service`

#### Tags

- Premium
- Corporate
- Balances
- Transactions

#### Properties

- [OpenAPI](openapi/danske-bank-uk-account-transaction-balance-premium-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Payment Collection API

Premium first-party corporate API for initiating and managing collection payment services, with a public mock sandbox.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://api.danskebank.com/corporate/api/v1/collection-service`

#### Tags

- Premium
- Corporate
- Payments
- Collections

#### Properties

- [OpenAPI](openapi/danske-bank-uk-payment-collection-premium-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) Premium Payment Initiation API

Premium first-party corporate payment initiation API for submitting and managing corporate payment orders, with a public mock sandbox.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://api.danskebank.com/corporate/api/v1/corporate-paymentorders`

#### Tags

- Premium
- Corporate
- Payments
- Payment Initiation

#### Properties

- [OpenAPI](openapi/danske-bank-uk-premium-payment-initiation-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) FX Trade Report API

Premium first-party API providing access to open and historical FX trade reports with filtering and pagination, with a public mock sandbox.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://api.danskebank.com/corporate/api/v1/open-trades-service`

#### Tags

- Premium
- Corporate
- FX
- Reporting

#### Properties

- [OpenAPI](openapi/danske-bank-uk-fx-trade-report-openapi.json)
- [Documentation](https://developers.danskebank.com/)

### Danske Bank (UK) FX Trade Execution API

Premium first-party API for executing FX trades against existing quotes, with a public mock sandbox.

- **Human URL:** [https://developers.danskebank.com/](https://developers.danskebank.com/)
- **Base URL:** `https://api.danskebank.com/corporate/api/v1/trade-service`

#### Tags

- Premium
- Corporate
- FX
- Trading

#### Properties

- [OpenAPI](openapi/danske-bank-uk-fx-trade-execution-openapi.json)
- [Documentation](https://developers.danskebank.com/)

## Common Properties

- [Website](https://www.danskebank.co.uk/)
- [Developer Portal](https://developers.danskebank.com/)
- [Documentation](https://developers.danskebank.com/documentation)
- [Getting Started](https://danskebank.co.uk/important-information/open-banking/third-party-providers)
- [Open Banking](https://danskebank.co.uk/important-information/open-banking)
- [Compliance / FCA Service Metrics](https://danskebank.co.uk/important-information/open-banking/api-data)
- [LinkedIn](https://www.linkedin.com/company/danske-bank)
- [Blog](https://danskebank.co.uk/about-us/news-and-insights)
- [Support](https://www.danskebank.co.uk/personal/help/useful-numbers)
- [Terms of Service](https://www.danskebank.co.uk/personal/terms-of-use)
- [Privacy Policy](https://www.danskebank.co.uk/personal/privacy-notice)
- [Cookies](https://www.danskebank.co.uk/personal/help/cookie-policy)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
