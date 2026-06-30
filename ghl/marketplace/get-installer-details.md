---
title: "Get Installer Details"
source_url: https://marketplace.gohighlevel.com/docs/ghl/marketplace/get-installer-details
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/marketplace/app/:appId/installations
summary: "Fetches installer details for the authenticated user. This endpoint returns information about the company, location, user, and installation details associated with the current OAuth token"
---
# Get Installer Details

```
GET https://services.leadconnectorhq.com/marketplace/app/:appId/installations
```


Fetches installer details for the authenticated user. This endpoint returns information about the company, location, user, and installation details associated with the current OAuth token.

### Requirements

#### Scope(s)

`marketplace-installer-details.readonly`

#### Auth Method(s)

`OAuth Access Token`

#### Token Type(s)

`Sub-Account Token``Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**appId** stringrequired

ID of the app to get installer details

Example: 6578278e879ad2646715ba9c

## Responses

- 200
- 400
- 403

Successfully retrieved installer details. Returns company, location, user, and installation information.

- application/json

- Schema
- Example (auto)

**Schema**

**installationDetails** object

Installation details

**companyId** stringrequired

Company ID

Example:`company123`

**locationId** string

Location ID (if applicable)

Example:`location123`

**companyName** stringrequired

Company name

Example:`Example Company`

**relationshipNumber** stringrequired

Company relationship number

Example:`0-002-230`

**companyEmail** stringnullable

Company email. Will be null for sub-account installations due to PII concerns.

Example:`contact@example.com`

**companyOwnerFullName** stringnullable

Company owner full name. Will be null for sub-account installations due to PII concerns.

Example:`John Doe`

**userId** stringrequired

User ID who installed the app

Example:`user123`

**isWhitelabelCompany** booleanrequired

Whether the company is a whitelabel company

Example:`false`

**companyPlan** stringnullable

Company plan. Will be null for sub-account installations due to business sensitivity.

Example:`agency_monthly_497`

**companyHighLevelPlan** stringnullabledeprecated

Company plan. Will be null for sub-account installations due to business sensitivity.

Example:`agency_monthly_497`

**marketplaceAppPlanId** string

Marketplace app plan ID for paid apps

Example:`plan123`

**whitelabelDetails** object

Whitelabel details (only present if isWhitelabelCompany is true)

**domain** stringrequired

Domain of the whitelabel company

Example:`example.com`

**logoUrl** stringrequired

Logo URL of the whitelabel company

Example:`https://example.com/logo.png`

```json
{
  "installationDetails": {
    "companyId": "company123",
    "locationId": "location123",
    "companyName": "Example Company",
    "relationshipNumber": "0-002-230",
    "companyEmail": "contact@example.com",
    "companyOwnerFullName": "John Doe",
    "userId": "user123",
    "isWhitelabelCompany": false,
    "companyPlan": "agency_monthly_497",
    "companyHighLevelPlan": "agency_monthly_497",
    "marketplaceAppPlanId": "plan123"
  }
}
```

Bad Request. Invalid request parameters or missing required data.

Forbidden. The client does not have necessary permissions to access installer details.

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: marketplace-installer-details.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account.
```

- curl
- nodejs
- python
- php
- java
- go
- ruby
- powershell

- CURL

```bash
curl -L 'https://services.leadconnectorhq.com/marketplace/app/:appId/installations' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-Access-OnlyAgency-Access-Only

Bearer Token

Parameters

appId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!