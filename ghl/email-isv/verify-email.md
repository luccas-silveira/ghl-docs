---
title: "Email Verification"
source_url: https://marketplace.gohighlevel.com/docs/ghl/email-isv/verify-email
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/email/verify
---
# Email Verification

```
POST https://services.leadconnectorhq.com/email/verify
```


Verify Email

### Requirements

#### Scope(s)

`lc-email.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/email-isv/verify-email/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Query Parameters

**locationId** stringrequired

Location Id, The email verification charges will be deducted from this location (if rebilling is enabled) / company wallet

Example: 5DP4iH6HLkQsiKESj6rh

- application/json

### Body **required**

**type** stringrequired

Email Verification type

**Possible values:** \[`email`, `contact`\]

Example:`email`

**verify** stringrequired

Email Verification recepient (email address / contactId)

Example:`abc@xyz.com`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/email-isv/verify-email/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

oneOf

- EmailVerifiedV3ResponseDto
- EmailNotVerifiedResponseDto
- LeadConnectorRecommendationDto

**reason** string\[\]

Reason for email verification failure

Example:`["mailbox_does_not_exist"]`

**result** stringrequired

Email verification result

**Possible values:** \[`deliverable`, `undeliverable`, `do_not_send`, `unknown`, `catch_all`\]

Example:`undeliverable`

**risk** stringrequired

Risk level of email sending to bounce

**Possible values:** \[`high`, `low`, `medium`, `unknown`\]

Example:`low`

**address** stringrequired

Email address

Example:`abc@xyz.com`

**leadConnectorRecommendation** object

Lead Connector email verification recommendation

**isEmailValid** boolean

Email verification status

Example:`false`

**verified** booleanrequired

Email verification not processed

Example:`false`

**message** string

Email verification failure message

Example:`Validation is disabled / proper config not found`

**address** string

Email address

Example:`abc@xyz.com`

**isEmailValid** boolean

Email verification status

Example:`false`

```json
{
  "reason": [\
    "mailbox_does_not_exist"\
  ],
  "result": "undeliverable",
  "risk": "low",
  "address": "abc@xyz.com",
  "leadConnectorRecommendation": {
    "isEmailValid": false
  }
}
```

Bad Request

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`400`

**message** string

Example:`Bad Request`

```json
{
  "statusCode": 400,
  "message": "Bad Request"
}
```

Unauthorized

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`401`

**message** string

Example:`Invalid token: access token is invalid`

**error** string

Example:`Unauthorized`

```json
{
  "statusCode": 401,
  "message": "Invalid token: access token is invalid",
  "error": "Unauthorized"
}
```

Unprocessable Entity

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`422`

**message** string\[\]

Example:`["Unprocessable Entity"]`

**error** string

Example:`Unprocessable Entity`

```json
{
  "statusCode": 422,
  "message": [\
    "Unprocessable Entity"\
  ],
  "error": "Unprocessable Entity"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: lc-email.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/email/verify' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
--data-raw '{
  "type": "email",
  "verify": "abc@xyz.com"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "type": "email",
  "verify": "abc@xyz.com"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!