---
title: "Get Access Token"
source_url: https://marketplace.gohighlevel.com/docs/ghl/oauth/get-access-token
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/oauth/token
summary: "Use Access Tokens to access CRM resources on behalf of an authenticated location/company"
---
# Get Access Token

```
POST https://services.leadconnectorhq.com/oauth/token
```


Use Access Tokens to access CRM resources on behalf of an authenticated location/company.

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

- application/x-www-form-urlencoded
- application/json

### Bodyrequired

**clientId** stringrequired

The ID provided by CRM for your integration

Example:`6578278e879ad2646715ba9c`

**clientSecret** stringrequired

The client secret provided by CRM for your integration

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**grantType** stringrequired

The OAuth2 grant type — authorization\_code, refresh\_token, or client\_credentials

**Possible values:** \[`authorization_code`, `refresh_token`, `client_credentials`\]

Example:`authorization_code`

**code** string

The authorization code received from the authorization endpoint (required for authorization\_code grant)

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**refreshToken** string

The refresh token used to obtain a new access token (required for refresh\_token grant)

Example:`xy34dc0ae1234a4858f9ff06d4f66ba`

**userType** string

The type of token to be requested

**Possible values:** \[`Company`, `Location`\]

Example:`Location`

**redirectUri** string

The redirect URI for your application

Example:`https://myapp.com/oauth/callback/crm`

### Bodyrequired

**clientId** stringrequired

The ID provided by CRM for your integration

Example:`6578278e879ad2646715ba9c`

**clientSecret** stringrequired

The client secret provided by CRM for your integration

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**grantType** stringrequired

The OAuth2 grant type — authorization\_code, refresh\_token, or client\_credentials

**Possible values:** \[`authorization_code`, `refresh_token`, `client_credentials`\]

Example:`authorization_code`

**code** string

The authorization code received from the authorization endpoint (required for authorization\_code grant)

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**refreshToken** string

The refresh token used to obtain a new access token (required for refresh\_token grant)

Example:`xy34dc0ae1234a4858f9ff06d4f66ba`

**userType** string

The type of token to be requested

**Possible values:** \[`Company`, `Location`\]

Example:`Location`

**redirectUri** string

The redirect URI for your application

Example:`https://myapp.com/oauth/callback/crm`

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

**accessToken** string

The OAuth2 access token

Example:`ab12dc0ae1234a7898f9ff06d4f69gh`

**tokenType** string

The token type (always Bearer)

Example:`Bearer`

**expiresIn** number

Time in seconds until the access token expires

Example:`86399`

**refreshToken** string

The OAuth2 refresh token used to obtain a new access token

Example:`xy34dc0ae1234a4858f9ff06d4f66ba`

**scope** string

Space-separated list of scopes the access token has access to

Example:`conversations/message.readonly conversations/message.write`

**userType** string

The user type associated with the token (Location or Company)

Example:`Location`

**locationId** string

Location ID - Present only for Sub-Account Access Token

Example:`l1C08ntBrFjLS0elLIYU`

**companyId** string

Company ID

Example:`l1C08ntBrFjLS0elLIYU`

**approvedLocations** string\[\]

Approved locations to generate location access token

Example:`["l1C08ntBrFjLS0elLIYU"]`

**userId** stringrequired

USER ID - Represent user id of person who performed installation

Example:`l1C08ntBrFjLS0elLIYU`

**planId** string

Plan Id of the subscribed plan in paid apps.

Example:`l1C08ntBrFjLS0elLIYU`

**isBulkInstallation** boolean

Indicates whether the installation was performed as a bulk installation

Example:`false`

**installToFutureLocations** boolean

Boolean to control if user wants app to be automatically installed to future locations (only for company tokens)

Example:`true`

**approveAllLocations** boolean

Boolean indicating if user approved all locations during bulk installation (only for company tokens)

Example:`true`

```json
{
  "accessToken": "ab12dc0ae1234a7898f9ff06d4f69gh",
  "tokenType": "Bearer",
  "expiresIn": 86399,
  "refreshToken": "xy34dc0ae1234a4858f9ff06d4f66ba",
  "scope": "conversations/message.readonly conversations/message.write",
  "userType": "Location",
  "locationId": "l1C08ntBrFjLS0elLIYU",
  "companyId": "l1C08ntBrFjLS0elLIYU",
  "approvedLocations": [\
    "l1C08ntBrFjLS0elLIYU"\
  ],
  "userId": "l1C08ntBrFjLS0elLIYU",
  "planId": "l1C08ntBrFjLS0elLIYU",
  "isBulkInstallation": false,
  "installToFutureLocations": true,
  "approveAllLocations": true
}
```

Bad Request

- application/json

- Schema
- Example (auto)
- invalidParameter
- missingParameter
- invalidRefreshToken
- locationNotActive

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

Thrown when any parameter (grantType, clientId, clientSecret, refreshToken, etc.) has an invalid value.

```json
{
  "statusCode": 400,
  "message": "Invalid parameter: grantType"
}
```

Thrown when a required parameter (grantType, clientId, clientSecret, refreshToken, etc.) is missing from the request.

```json
{
  "statusCode": 400,
  "message": "Missing parameter: clientId"
}
```

Thrown when the supplied refresh token is invalid, expired, or has already been used.

```json
{
  "statusCode": 400,
  "message": "Invalid grant: refresh token is invalid"
}
```

Thrown when the location is not active (Due to SaaS subscription incomplete, paused, canceled, etc. Agency manually paused location. Agency becomes inactive.). Once the location becomes active again, the same refresh token can be used to get a new access token, provided the app is still installed on the location.

```json
{
  "statusCode": 400,
  "message": "Location is not active"
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
curl -L -X POST 'https://services.leadconnectorhq.com/oauth/token' \
-H 'Content-Type: application/x-www-form-urlencoded' \
-H 'Accept: application/json'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

Version — headerrequired

\-\-\-v3

Body required

Content-Type

application/x-www-form-urlencodedapplication/json

clientIdrequired

clientSecretrequired

grantTyperequired

\-\-\-authorization\_coderefresh\_tokenclient\_credentials

code

refreshToken

userType

\-\-\-CompanyLocation

redirectUri

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!