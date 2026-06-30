---
title: "Add Contact to Campaign"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/add-contact-to-campaign
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/contacts/:contactId/campaigns/:campaignId
---
# Add Contact to Campaign

```
POST https://services.leadconnectorhq.com/contacts/:contactId/campaigns/:campaignId
```


Add contact to Campaign

### Requirements

#### Scope(s)

`contacts.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/add-contact-to-campaign/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**contactId** stringrequired

Contact Id

Example: ve9EPM428h8vShlRW1KT

**campaignId** stringrequired

Campaign Id

Example: Y5AMhDEE4L6EuVmmDTKZ

- application/json

### Body **required**

object

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/add-contact-to-campaign/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**succeeded** boolean

Whether the campaign operation was successful

Example:`true`

**succeded** booleandeprecated

Legacy misspelling of `succeeded`. Deprecated; use `succeeded`.

Example:`true`

```json
{
  "succeeded": true
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
name: Authorizationtype: httpscopes: contacts.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/contacts/:contactId/campaigns/:campaignId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

contactId — pathrequired

campaignId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!