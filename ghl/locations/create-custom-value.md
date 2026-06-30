---
title: "Create Custom Value"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/create-custom-value
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/locations/:locationId/customValues
---
# Create Custom Value

```
POST https://services.leadconnectorhq.com/locations/:locationId/customValues
```

Create Custom Value

### Requirements

#### Scope(s)

`locations/customValues.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/locations/create-custom-value/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

- application/json

### Body **required**

**name** stringrequired

Example:`Custom Field Name`

**value** stringrequired

Example:`Value`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/locations/create-custom-value/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**customValue** object

**id** string

Example:`rWQ709Pb62syqGLceg1x`

**name** string

Example:`Custom Field`

**fieldKey** string

Example:`{{ custom_values.custom_field }}`

**value** string

Example:`Value`

**locationId** string

Example:`rWQ709Pb6dasyqGLceg1x`

```json
{
  "customValue": {
    "id": "rWQ709Pb62syqGLceg1x",
    "name": "Custom Field",
    "fieldKey": "{{ custom_values.custom_field }}",
    "value": "Value",
    "locationId": "rWQ709Pb6dasyqGLceg1x"
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
name: Authorizationtype: httpscopes: locations/customValues.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "Custom Field Name",
  "value": "Value"
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
  "name": "Custom Field Name",
  "value": "Value"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!