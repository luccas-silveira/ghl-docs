---
title: "List Payouts"
source_url: https://marketplace.gohighlevel.com/docs/ghl/affiliate-manager/list-payouts
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/affiliate-manager/:locationId/payouts
summary: "Retrieve the list of payouts for a location"
---
# List Payouts

```
GET https://services.leadconnectorhq.com/affiliate-manager/:locationId/payouts
```


Retrieve the list of payouts for a location.

### Requirements

#### Scope(s)

`affiliate-manager.readonly`

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

Location Id

Example: ve9EPM428h8vShlRW1KT

### Query Parameters

**status** string

Payout status

Example: pending

**query** string

query

Example: john

**affiliateId** string

Affiliate Id

Example: 65df04201e428a0c5ebb6572

**campaignId** string

Campaign Id

Example: 65df04201e428a0c5ebb6573

**skip** number

Default value:`0`

Example: 1

**limit** number

Default value:`10`

Example: 10

**start** string

Example: 2022-12-01T00:00:00.000Z

**end** string

Example: 2022-12-31T23:59:59.999Z

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

**payouts** object\[\]required

Payout list

Array \[\
\
**\_id** stringrequired\
\
Payout id\
\
Example:`65df04201e428a0c5ebb6571`\
\
**locationId** stringrequired\
\
Location id\
\
Example:`ve9EPM428h8vShlRW1KT`\
\
**affiliateId** stringrequired\
\
Affiliate id\
\
Example:`65df04201e428a0c5ebb6572`\
\
**campaignId** string\
\
Campaign id\
\
Example:`65df04201e428a0c5ebb6573`\
\
**currency** stringrequired\
\
Payout currency\
\
Example:`USD`\
\
**amount** numberrequired\
\
Payout amount\
\
Example:`150`\
\
**status** string\
\
Payout status\
\
Example:`pending`\
\
**payoutMonth** string\
\
Payout month\
\
Example:`2024-06-01T00:00:00.000Z`\
\
**dueAt** string\
\
Payout due date\
\
Example:`2024-06-30T00:00:00.000Z`\
\
**paidAt** string\
\
Payout paid date\
\
Example:`2024-06-30T00:00:00.000Z`\
\
**paidMeta** object\
\
Payout metadata\
\
**paidMethod** string\
\
Payout paid method\
\
Example:`manual`\
\
**altId** string\
\
Alternate id\
\
Example:`alt_123`\
\
**deleted** boolean\
\
Whether the payout is deleted\
\
Example:`false`\
\
**isMigrated** boolean\
\
Whether the payout is migrated\
\
Example:`false`\
\
**createdAt** string\
\
Created at timestamp\
\
Example:`2024-06-16T00:00:00.000Z`\
\
**updatedAt** string\
\
Updated at timestamp\
\
Example:`2024-06-17T00:00:00.000Z`\
\
**campaign** string\
\
Campaign name\
\
Example:`Summer Promo`\
\
**affiliateName** string\
\
Affiliate display name\
\
Example:`John Doe`\
\
**affiliateEmail** string\
\
Affiliate email\
\
Example:`john.doe@example.com`\
\
**payoutMethod** string\
\
Primary payout method\
\
Example:`paypal`\
\
**affiliate** object\
\
Affiliate details\
\
**\_id** stringrequired\
\
Affiliate id\
\
Example:`63d147176c5bbc30e9e091a4`\
\
**firstName** string\
\
Affiliate first name\
\
Example:`John`\
\
**lastName** string\
\
Affiliate last name\
\
Example:`Doe`\
\
**phone** string\
\
Affiliate phone number\
\
Example:`+1 888 888-8888`\
\
**deleted** boolean\
\
Whether the affiliate is deleted\
\
Example:`false`\
\
**locationId** stringrequired\
\
Location id\
\
Example:`ve9EPM428h8vShlRW1KT`\
\
**active** boolean\
\
Whether the affiliate is active\
\
Example:`true`\
\
**address** string\
\
Affiliate address\
\
Example:`123 Main St`\
\
**avatar** string\
\
Affiliate avatar URL\
\
Example:`https://example.com/avatar.png`\
\
**createdAt** string\
\
Created at timestamp\
\
Example:`2024-06-16T00:00:00.000Z`\
\
**createdBy** object\
\
Created by audit info\
\
**facebookUrl** string\
\
Facebook URL\
\
Example:`https://facebook.com/johndoe`\
\
**instagramUrl** string\
\
Instagram URL\
\
Example:`https://instagram.com/johndoe`\
\
**linkedInUrl** string\
\
LinkedIn URL\
\
Example:`https://linkedin.com/in/johndoe`\
\
**twitterUrl** string\
\
Twitter URL\
\
Example:`https://twitter.com/johndoe`\
\
**youtubeUrl** string\
\
YouTube URL\
\
Example:`https://youtube.com/channel`\
\
**websiteUrl** string\
\
Website URL\
\
Example:`https://example.com`\
\
**contactId** string\
\
Contact id associated with the affiliate\
\
Example:`ve9EPM428h8vShlRW1KT`\
\
**campaignIds** string\[\]\
\
Campaign ids\
\
Example:`["650173614761b33c46d33b19"]`\
\
**vatId** string\
\
VAT ID\
\
Example:`VAT123`\
\
**updatedAt** string\
\
Updated at timestamp\
\
Example:`2024-06-16T00:00:00.000Z`\
\
**w8Form** string\
\
W8 form URL\
\
**w9Form** string\
\
W9 form URL\
\
**lastUpdatedBy** object\
\
Last updated by audit info\
\
**email** stringrequired\
\
Affiliate email\
\
Example:`john.doe@example.com`\
\
**revenue** number\
\
Affiliate revenue\
\
Example:`1250.5`\
\
**customer** number\
\
Customer count\
\
Example:`15`\
\
**lead** number\
\
Lead count\
\
Example:`5`\
\
**droppedCustomer** number\
\
Dropped customer count\
\
Example:`2`\
\
**clickCount** number\
\
Click count\
\
Example:`100`\
\
**paid** number\
\
Paid amount\
\
Example:`500`\
\
**currency** string\
\
Currency code\
\
Example:`USD`\
\
**owned** number\
\
Owned amount\
\
Example:`750`\
\
\]

**meta** object

Pagination metadata

**count** numberrequired

Total payouts matching the filters

Example:`42`

```json
{
  "payouts": [\
    {\
      "_id": "65df04201e428a0c5ebb6571",\
      "locationId": "ve9EPM428h8vShlRW1KT",\
      "affiliateId": "65df04201e428a0c5ebb6572",\
      "campaignId": "65df04201e428a0c5ebb6573",\
      "currency": "USD",\
      "amount": 150,\
      "status": "pending",\
      "payoutMonth": "2024-06-01T00:00:00.000Z",\
      "dueAt": "2024-06-30T00:00:00.000Z",\
      "paidAt": "2024-06-30T00:00:00.000Z",\
      "paidMeta": {},\
      "paidMethod": "manual",\
      "altId": "alt_123",\
      "deleted": false,\
      "isMigrated": false,\
      "createdAt": "2024-06-16T00:00:00.000Z",\
      "updatedAt": "2024-06-17T00:00:00.000Z",\
      "campaign": "Summer Promo",\
      "affiliateName": "John Doe",\
      "affiliateEmail": "john.doe@example.com",\
      "payoutMethod": "paypal",\
      "affiliate": {\
        "_id": "63d147176c5bbc30e9e091a4",\
        "firstName": "John",\
        "lastName": "Doe",\
        "phone": "+1 888 888-8888",\
        "deleted": false,\
        "locationId": "ve9EPM428h8vShlRW1KT",\
        "active": true,\
        "address": "123 Main St",\
        "avatar": "https://example.com/avatar.png",\
        "createdAt": "2024-06-16T00:00:00.000Z",\
        "createdBy": {},\
        "facebookUrl": "https://facebook.com/johndoe",\
        "instagramUrl": "https://instagram.com/johndoe",\
        "linkedInUrl": "https://linkedin.com/in/johndoe",\
        "twitterUrl": "https://twitter.com/johndoe",\
        "youtubeUrl": "https://youtube.com/channel",\
        "websiteUrl": "https://example.com",\
        "contactId": "ve9EPM428h8vShlRW1KT",\
        "campaignIds": [\
          "650173614761b33c46d33b19"\
        ],\
        "vatId": "VAT123",\
        "updatedAt": "2024-06-16T00:00:00.000Z",\
        "w8Form": "string",\
        "w9Form": "string",\
        "lastUpdatedBy": {},\
        "email": "john.doe@example.com",\
        "revenue": 1250.5,\
        "customer": 15,\
        "lead": 5,\
        "droppedCustomer": 2,\
        "clickCount": 100,\
        "paid": 500,\
        "currency": "USD",\
        "owned": 750\
      }\
    }\
  ],
  "meta": {
    "count": 42
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
name: Authorizationtype: httpscopes: affiliate-manager.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/affiliate-manager/:locationId/payouts' \
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

Show optional parameters

status — query

query — query

affiliateId — query

campaignId — query

skip — query

limit — query

start — query

end — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!