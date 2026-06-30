---
title: "Get Custom Values"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/get-custom-values
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/locations/:locationId/customValues
---
# Get Custom Values

```
GET https://services.leadconnectorhq.com/locations/:locationId/customValues
```

Get Custom Values

### Requirements

#### Scope(s)

`locations/customValues.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**customValues** object\[\]

Array \[\
\
**id** string\
\
Example:`rWQ709Pb62syqGLceg1x`\
\
**name** string\
\
Example:`Custom Field`\
\
**fieldKey** string\
\
Example:`{{ custom_values.custom_field }}`\
\
**value** string\
\
Example:`Value`\
\
**locationId** string\
\
Example:`rWQ709Pb6dasyqGLceg1x`\
\
\]

```json
{
  "customValues": [\
    {\
      "id": "rWQ709Pb62syqGLceg1x",\
      "name": "Custom Field",\
      "fieldKey": "{{ custom_values.custom_field }}",\
      "value": "Value",\
      "locationId": "rWQ709Pb6dasyqGLceg1x"\
    }\
  ]
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: locations/customValues.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/locations/:locationId/customValues' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
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

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!