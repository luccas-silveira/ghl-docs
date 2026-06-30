---
title: "Delete Product by ID"
source_url: https://marketplace.gohighlevel.com/docs/ghl/products/delete-product-by-id
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/products/:productId
summary: "The 'Delete Product by ID' API allows deleting a specific product using its unique identifier. Use this endpoint to remove a product from the system"
---
# Delete Product by ID

```
DELETE https://services.leadconnectorhq.com/products/:productId
```


The "Delete Product by ID" API allows deleting a specific product using its unique identifier. Use this endpoint to remove a product from the system.

### Requirements

#### Scope(s)

`products.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token``Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**productId** stringrequired

ID or the slug of the product that needs to be returned

Example: 6578278e879ad2646715ba9c

### Query Parameters

**locationId** stringrequired

location Id

Example: 6578278e879ad2646715ba9c

**sendWishlistStatus** boolean

Parameter which will decide whether to show the wishlisting status of products

Example:

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

**status** booleanrequired

returns true if the product is successfully deleted

Example:`true`

```json
{
  "status": true
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
name: Authorizationtype: httpscopes: products.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/products/:productId' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-AccessAgency-Access

Bearer Token

Parameters

productId — pathrequired

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

sendWishlistStatus — query

\-\-\-truefalse

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!