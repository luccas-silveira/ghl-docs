---
title: "Import an email template"
source_url: https://marketplace.gohighlevel.com/docs/ghl/emails/import-email-template
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/emails/locations/:locationId/templates/import
---
# Import an email template

```
POST https://services.leadconnectorhq.com/emails/locations/:locationId/templates/import
```


Import a template from a provider URL

### Requirements

#### Scope(s)

`emails/templates.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/emails/import-email-template/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**locationId** stringrequired

Location ID

Example: ve9EPM428h8vShlRW1KT

- application/json

### Body **required**

**importProvider** stringrequired

Import provider (URL-based providers only)

**Possible values:** \[`mailchimp`, `active_campaign`\]

Example:`mailchimp`

**importUrl** stringrequired

Public import URL

Example:`https://templates.example.com/public/template-123`

**name** string

Template name

Example:`Imported Template`

**parentFolderId** string

Parent folder ID

Example:`67f15c2ae99226d5bcccb8f0`

**userId** string

ID of the user performing this action

Example:`507f1f77bcf86cd799439011`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/emails/import-email-template/\#responses "Direct link to Responses")

- 201
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

Template ID

Example:`507f1f77bcf86cd799439011`

**name** stringrequired

Template name

Example:`Newsletter Template`

**editorType** stringrequired

Editor type

**Possible values:** \[`html`, `text`\]

Example:`html`

**isPlainText** booleanrequired

Whether template is plain text

Example:`false`

**parentFolderId** string

Parent folder ID

Example:`67f15c2ae99226d5bcccb8f0`

**fromName** string

Sender name

Example:`John Doe`

**fromEmail** string

Sender email address

Example:`john@example.com`

**subjectLine** string

Email subject line

Example:`Welcome to our newsletter`

**previewText** string

Preview text

Example:`Email preview text`

**previewUrl** string

Preview URL

Example:`https://example.com/preview/template123`

**createdAt** string

Created timestamp

Example:`2025-07-24T11:55:43.598Z`

**updatedAt** string

Updated timestamp

Example:`2025-07-24T11:55:43.598Z`

**traceId** string

Trace ID of request

Example:`019e4ef5-a65e-4198-8cf9-8e93dca9bda4`

```json
{
  "id": "507f1f77bcf86cd799439011",
  "name": "Newsletter Template",
  "editorType": "html",
  "isPlainText": false,
  "parentFolderId": "67f15c2ae99226d5bcccb8f0",
  "fromName": "John Doe",
  "fromEmail": "john@example.com",
  "subjectLine": "Welcome to our newsletter",
  "previewText": "Email preview text",
  "previewUrl": "https://example.com/preview/template123",
  "createdAt": "2025-07-24T11:55:43.598Z",
  "updatedAt": "2025-07-24T11:55:43.598Z",
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
name: Authorizationtype: httpscopes: emails/templates.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/emails/locations/:locationId/templates/import' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "importProvider": "mailchimp",
  "importUrl": "https://templates.example.com/public/template-123",
  "name": "Imported Template",
  "parentFolderId": "67f15c2ae99226d5bcccb8f0",
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

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "importProvider": "mailchimp",
  "importUrl": "https://templates.example.com/public/template-123",
  "name": "Imported Template",
  "parentFolderId": "67f15c2ae99226d5bcccb8f0",
  "userId": "507f1f77bcf86cd799439011"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!