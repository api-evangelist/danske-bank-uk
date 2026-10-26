# Danske Bank (UK) (danske-bank-uk)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
