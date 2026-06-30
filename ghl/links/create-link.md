---
title: "Create Link"
source_url: https://marketplace.gohighlevel.com/docs/ghl/links/create-link
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/links
summary: "Location ID of the business profile"
---
# Create Link

```
POST https://services.leadconnectorhq.com/links/
```


Create Link

### Requirements

#### Scope(s)

`links.write`

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

- application/json

### Body **required**

**locationId** stringrequired

Location ID of the business profile

Example:`ve9EPM428h8vShlRW1KT`

**name** stringrequired

Display name of the trigger link

Example:`first tag`

**redirectTo** stringrequired

URL or variable to redirect to when the trigger link is clicked

Example:`https://www.google.com/`

## Responses

- 201
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**link** object

The trigger link object

**id** string

Unique identifier of the trigger link

Example:`n4AriwEnFrGh3tu08W0U`

**name** string

Display name of the trigger link

Example:`first tag`

**redirectTo** string

URL or variable to redirect to when the trigger link is clicked

Example:`https://www.google.com/`

**fieldKey** string

Template variable key used to reference this trigger link

Example:`{{trigger_link.n4AriwEnFrGh3tu08W0U}}`

**locationId** string

Location ID this trigger link belongs to

Example:`ve9EPM428h8vShlRW1KT`

```json
{
  "link": {
    "id": "n4AriwEnFrGh3tu08W0U",
    "name": "first tag",
    "redirectTo": "https://www.google.com/",
    "fieldKey": "{{trigger_link.n4AriwEnFrGh3tu08W0U}}",
    "locationId": "ve9EPM428h8vShlRW1KT"
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
name: Authorizationtype: httpscopes: links.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/links/' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "ve9EPM428h8vShlRW1KT",
  "name": "first tag",
  "redirectTo": "https://www.google.com/"
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
  "locationId": "ve9EPM428h8vShlRW1KT",
  "name": "first tag",
  "redirectTo": "https://www.google.com/"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!