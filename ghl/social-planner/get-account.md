---
title: "Get Accounts"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/get-account
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/accounts
summary: "Get list of accounts and groups"
---
# Get Accounts

```
GET https://services.leadconnectorhq.com/social-media-posting/:locationId/accounts
```


Get list of accounts and groups

### Requirements

#### Scope(s)

`socialplanner/account.readonly`

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

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Accounts`

**results** object

Requested Results

**accounts** object\[\]

Array of connected social media accounts

Array \[\
\
**id** string\
\
Unique identifier for the connected account\
\
Example:`aF3KhyL8JIuBwzK3m7Ly_Lx1EI6YIgQYMQi0ytFXv_12554616564525983496`\
\
**oauthId** string\
\
OAuth provider account identifier\
\
Example:`aF3KhyL8JIuBwzK3m7Ly`\
\
**profileId** string\
\
Profile identifier from the social media platform\
\
Example:`aF3KhyL8JIuBwzK3m7Ly`\
\
**name** string\
\
Display name of the account\
\
Example:`Sample Account`\
\
**platform** string\
\
platform must be one of the following values: google, facebook, instagram, linkedin, tiktok\
\
Example:`google`\
\
**type** string\
\
Type of account (e.g., location, page, profile)\
\
Example:`location`\
\
**expire** string\
\
Token expiration date and time\
\
Example:`2024-03-11T19:29:59.785Z`\
\
**isExpired** boolean\
\
Indicates if the account token has expired\
\
Example:`false`\
\
**meta** object\
\
Additional metadata for the account\
\
Example:`{"hasGoogleUpdated":true,"canDelete":true}`\
\
\]

**groups** object\[\]

Array of account groups

Array \[\
\
**id** stringrequired\
\
Group Id\
\
Example:`6284c43d519161e96cc09c13`\
\
**name** stringrequired\
\
name of group\
\
Example:`Primary`\
\
**accountIds** string\[\]required\
\
Array of account IDs belonging to this group\
\
Example:`["6494063f4260855c1c5776b5_mhoUgTPkz19vjF5Qu7Av_2774080328752823730"]`\
\
\]

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Accounts",
  "results": {
    "accounts": [\
      {\
        "id": "aF3KhyL8JIuBwzK3m7Ly_Lx1EI6YIgQYMQi0ytFXv_12554616564525983496",\
        "name": "Sample Account",\
        "platform": "google"\
      }\
    ],
    "groups": [\
      {\
        "id": "6284c43d519161e96cc09c13",\
        "name": "Primary"\
      }\
    ]
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
name: Authorizationtype: httpscopes: socialplanner/account.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/:locationId/accounts' \
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