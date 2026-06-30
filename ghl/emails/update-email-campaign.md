---
title: "Update Email Campaign"
source_url: https://marketplace.gohighlevel.com/docs/ghl/emails/update-email-campaign
version: v3
method: PATCH
endpoint: https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/emails/:campaignId
summary: "Update an email campaign draft"
---
# Update Email Campaign

```
PATCH https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/emails/:campaignId
```

Update an email campaign draft

### Requirements

#### Scope(s)

`emails/campaigns.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**locationId** stringrequired

Location ID

Example: ve9EPM428h8vShlRW1KT

**campaignId** stringrequired

Campaign ID

Example: 67f15c2ae99226d5bcccb8f3

- application/json

### Body **required**

**name** string

Campaign name

Example:`Untitled campaign name`

**editorContent** string

Editor content to update. Required only when updating campaign content, and must be provided together with editorType. Provide HTML or plain-text string content.

Example:`<html><body>Hello World</body></html>`

**editorType** string

Editor type for campaign content. Required only when updating campaign content, and must be provided together with editorContent.

**Possible values:** \[`html`, `text`\]

Example:`html`

**userId** string

ID of the user performing this action

Example:`507f1f77bcf86cd799439011`

## Responses

- 200
- 400
- 401
- 403
- 404
- 422

Success

- application/json

- Schema
- Example (auto)

**Schema**

**id** stringrequired

Campaign ID

Example:`67f15c2ae99226d5bcccb8f3`

**source** string

Source of the campaign

Example:`email-campaign`

**sourceId** string

Source ID of the campaign

Example:`bulkRequest_abc123`

**name** string

Campaign name

Example:`February Newsletter`

**status** string

Campaign status

**Possible values:** \[`all`, `sent`, `failed`, `archived`, `draft`, `processing`, `scheduled`, `cancelled`, `paused`\]

Example:`sent`

**campaignType** string

Campaign type

Example:`bulk-email`

**campaignCategory** string

Campaign category

Example:`email-campaign`

**variations** object\[\]

AB test variation identifiers (available only for AB test campaigns)

Array \[\
\
**sourceId** stringrequired\
\
Variation source ID for stats lookup\
\
Example:`9MhVcU7dTdLI7XOU1Vdt`\
\
**isWinner** booleanrequired\
\
Whether this is the winning variation\
\
Example:`true`\
\
\]

**deleted** booleanrequired

Whether the campaign is deleted

Example:`false`

**createdAt** stringrequired

Created at timestamp

Example:`2025-07-24T11:55:43.598Z`

**updatedAt** stringrequired

Last updated timestamp

Example:`2026-02-09T04:49:12.322Z`

**traceId** string

Trace ID of request

Example:`019e4ef5-a65e-4198-8cf9-8e93dca9bda4`

```json
{
  "id": "67f15c2ae99226d5bcccb8f3",
  "source": "email-campaign",
  "sourceId": "bulkRequest_abc123",
  "name": "February Newsletter",
  "status": "sent",
  "campaignType": "bulk-email",
  "campaignCategory": "email-campaign",
  "variations": [\
    {\
      "sourceId": "9MhVcU7dTdLI7XOU1Vdt",\
      "isWinner": true\
    }\
  ],
  "deleted": false,
  "createdAt": "2025-07-24T11:55:43.598Z",
  "updatedAt": "2026-02-09T04:49:12.322Z",
  "traceId": "019e4ef5-a65e-4198-8cf9-8e93dca9bda4"
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

The token does not have access to this location

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

HTTP status code for invalid location access

Example:`403`

**message** string

Error message describing the location access failure

Example:`The token does not have access to this location`

```json
{
  "statusCode": 403,
  "message": "The token does not have access to this location"
}
```

Not Found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

HTTP status code for not found

Example:`404`

**message** string

Error message describing the not found failure

Example:`Not Found`

**error** string

Error type identifier

Example:`The requested resource was not found`

```json
{
  "statusCode": 404,
  "message": "Not Found",
  "error": "The requested resource was not found"
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
name: Authorizationtype: httpscopes: emails/campaigns.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PATCH 'https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/emails/:campaignId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "Untitled campaign name",
  "editorContent": "<html><body>Hello World</body></html>",
  "editorType": "html",
  "userId": "507f1f77bcf86cd799439011"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

locationId — pathrequired

campaignId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "name": "Untitled campaign name",
  "editorContent": "<html><body>Hello World</body></html>",
  "editorType": "html",
  "userId": "507f1f77bcf86cd799439011"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!