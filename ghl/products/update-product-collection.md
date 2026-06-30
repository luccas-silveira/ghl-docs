---
title: "Update Product Collection"
source_url: https://marketplace.gohighlevel.com/docs/ghl/products/update-product-collection
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/products/collections/:collectionId
---
# Update Product Collection

```
PUT https://services.leadconnectorhq.com/products/collections/:collectionId
```


Update a specific product collection with Id :collectionId

### Requirements

#### Scope(s)

`products/collection.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/products/update-product-collection/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**collectionId** stringrequired

MongoId of the collection

Example: 65d71377c326ea78e1c47df5

- application/json

### Body **required**

**altId** stringrequired

Location Id

Example:`6578278e879ad2646715ba9c`

**altType** stringrequired

The type of alt. For now it is only LOCATION

**Possible values:** \[`location`\]

Example:`LOCATION`

**name** string

Name of the Product Collection

Example:`Best Sellers`

**slug** string

Slug of the Product Collection which helps in navigation

Example:`best-sellers`

**image** string

The URL of the image that is going to be displayed as the collection Thumbnail

Example:`http://example.com/watermark.png`

**seo** object

The metadata information which will be displayed in SEO previews

**title** string

The title which will be displayed as an SEO format

Example:`Best Sellers`

**description** string

The description which would be displayed in preview purposes

Example:`Collections where all the best products are available`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/products/update-product-collection/\#responses "Direct link to Responses")

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

Status of api action

Example:`true`

**message** string

Success message

Example:`Successfully created`

```json
{
  "status": true,
  "message": "Successfully created"
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
name: Authorizationtype: httpscopes: products/collection.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/products/collections/:collectionId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "altId": "6578278e879ad2646715ba9c",
  "altType": "LOCATION",
  "name": "Best Sellers",
  "slug": "best-sellers",
  "image": "http://example.com/watermark.png",
  "seo": {
    "title": "Best Sellers",
    "description": "Collections where all the best products are available"
  }
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

collectionId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "altId": "6578278e879ad2646715ba9c",
  "altType": "LOCATION",
  "name": "Best Sellers",
  "slug": "best-sellers",
  "image": "http://example.com/watermark.png",
  "seo": {
    "title": "Best Sellers",
    "description": "Collections where all the best products are available"
  }
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!