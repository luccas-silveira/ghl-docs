---
title: "Create Custom Field Folder"
source_url: https://marketplace.gohighlevel.com/docs/ghl/custom-fields/create-custom-field-folder
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/custom-fields/folder
---
# Create Custom Field Folder

```
POST https://services.leadconnectorhq.com/custom-fields/folder
```


Create Custom Field Folder

info

Only supports Custom Objects and Company (Business) today. Will be extended to other Standard Objects in the future.

### Requirements

#### Scope(s)

`locations/customFields.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/custom-fields/create-custom-field-folder/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- application/json

### Body **required**

**objectKey** stringrequired

The key for your custom object. This key uniquely identifies the custom object. Example: "custom\_object.pet" for a custom object related to pets.

Example:`custom_object.pet`

**name** stringrequired

Field name

Example:`Name`

**locationId** stringrequired

Location Id

Example:`ve9EPM428h8vShlRW1KT`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/custom-fields/create-custom-field-folder/\#responses "Direct link to Responses")

- 201
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**id** stringrequired

Unique identifier of the object

**objectKey** stringrequired

The key for your custom object. This key uniquely identifies the custom object. Example: "custom\_object.pet" for a custom object related to pets.

Example:`custom_object.pet`

**locationId** stringrequired

Location Id

Example:`ve9EPM428h8vShlRW1KT`

**name** stringrequired

Field name

Example:`Name`

```json
{
  "id": "string",
  "objectKey": "custom_object.pet",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "name": "Name"
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
name: Authorizationtype: httpscopes: locations/customFields.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/custom-fields/folder' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "objectKey": "custom_object.pet",
  "name": "Name",
  "locationId": "ve9EPM428h8vShlRW1KT"
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
  "objectKey": "custom_object.pet",
  "name": "Name",
  "locationId": "ve9EPM428h8vShlRW1KT"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!