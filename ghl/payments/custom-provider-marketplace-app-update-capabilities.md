---
title: "Custom-provider marketplace app update capabilities"
source_url: https://marketplace.gohighlevel.com/docs/ghl/payments/custom-provider-marketplace-app-update-capabilities
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/payments/custom-provider/capabilities
summary: "Toggle capabilities for the marketplace app tied to the OAuth client"
---
# Custom-provider marketplace app update capabilities

```
PUT https://services.leadconnectorhq.com/payments/custom-provider/capabilities
```

Toggle capabilities for the marketplace app tied to the OAuth client

### Requirements

#### Scope(s)

`payments/custom-provider.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- application/json

### Body **required**

**supportsSubscriptionSchedules** booleanrequired

Whether the marketplace app supports subscription schedules or not

Example:`true`

**companyId** string

Company id. Mandatory if locationId is not provided

Example:`Yjnwuduw83e8x30sm0`

**locationId** string

Location / Sub-account id. Mandatory if companyId is not provided

Example:`Yjnwuduw83e8x30sm0`

## Responses

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Whether the custom provider capabilities are updated or not. true represents capabilities are updated

Example:`true`

```json
{
  "success": "true"
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
name: Authorizationtype: httpscopes: payments/custom-provider.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/payments/custom-provider/capabilities' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "supportsSubscriptionSchedules": true,
  "companyId": "Yjnwuduw83e8x30sm0",
  "locationId": "Yjnwuduw83e8x30sm0"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "supportsSubscriptionSchedules": true,
  "companyId": "Yjnwuduw83e8x30sm0",
  "locationId": "Yjnwuduw83e8x30sm0"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!