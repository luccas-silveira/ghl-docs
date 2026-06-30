---
title: "Get Location Access Token from Agency Token"
source_url: https://marketplace.gohighlevel.com/docs/ghl/oauth/get-location-access-token
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/oauth/location-token
---
# Get Location Access Token from Agency Token

```
POST https://services.leadconnectorhq.com/oauth/location-token
```


This API allows you to generate locationAccessToken from AgencyAccessToken

### Requirements

#### Scope(s)

`oauth.write`

#### Auth Method(s)

`OAuth Access Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/oauth/get-location-access-token/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

- application/x-www-form-urlencoded

### Body **required**

**companyId** stringrequired

Company Id of location you want to request token for

Example:`tDtDnQdgm2LXpyiqYvZ6`

**locationId** stringrequired

The location ID for which you want to obtain accessToken

Example:`l1C08ntBrFjLS0elLIYU`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/oauth/get-location-access-token/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**accessToken** string

Location access token which can be used to authenticate & authorize API under following scope

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**tokenType** string

The token type (always Bearer)

Example:`Bearer`

**expiresIn** number

Time in seconds remaining for token to expire

Example:`86399`

**scope** string

Scopes the following accessToken have access to

Example:`conversations/message.readonly conversations/message.write`

**locationId** string

Location ID - Present only for Sub-Account Access Token

Example:`l1C08ntBrFjLS0elLIYU`

**planId** string

Plan Id of the subscribed plan in paid apps.

Example:`l1C08ntBrFjLS0elLIYU`

**userId** stringrequired

USER ID - Represent user id of person who performed installation

Example:`l1C08ntBrFjLS0elLIYU`

**appId** string

App ID of the installed application

Example:`6578278e879ad2646715ba9c`

**versionId** string

Version ID of the installed app version

Example:`6578278e879ad2646715ba9c`

**refreshToken** string

The OAuth2 refresh token used to obtain a new access token for this specific location.

Example:`eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWUsImlhdCI6MTUxNjIzOTAyMn0.KMUFsIDTnFmyG3nMiGM6H9FNFUROf3wh7SmqJp-QV30`

```json
{
  "accessToken": "ab12dc0ae1234a7898f9ff06d4f69gh",
  "tokenType": "Bearer",
  "expiresIn": 86399,
  "scope": "conversations/message.readonly conversations/message.write",
  "locationId": "l1C08ntBrFjLS0elLIYU",
  "planId": "l1C08ntBrFjLS0elLIYU",
  "userId": "l1C08ntBrFjLS0elLIYU",
  "appId": "6578278e879ad2646715ba9c",
  "versionId": "6578278e879ad2646715ba9c",
  "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWUsImlhdCI6MTUxNjIzOTAyMn0.KMUFsIDTnFmyG3nMiGM6H9FNFUROf3wh7SmqJp-QV30"
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
name: Authorizationtype: httpscopes: oauth.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency.
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
curl -L -X POST 'https://services.leadconnectorhq.com/oauth/location-token' \
-H 'Content-Type: application/x-www-form-urlencoded' \
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

Version — headerrequired

\-\-\-v3

Body required

companyIdrequired

locationIdrequired

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!