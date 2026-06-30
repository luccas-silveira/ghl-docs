---
title: "Uninstall an application"
source_url: https://marketplace.gohighlevel.com/docs/ghl/marketplace/uninstall-application
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/marketplace/app/:appId/installations
summary: "Uninstalls an application from your company or a specific location. This will remove the application\`s access and stop all its functionalities"
---
# Uninstall an application

```
DELETE https://services.leadconnectorhq.com/marketplace/app/:appId/installations
```


Uninstalls an application from your company or a specific location. This will remove the application\`s access and stop all its functionalities

### Requirements

#### Scope(s)

`oauth.write`

#### Auth Method(s)

`OAuth Access Token`

#### Token Type(s)

`Sub-Account Token``Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**appId** stringrequired

The application id which is to be uninstalled.

Example: 674587703dfd4161f1e3c557

- application/json

### Body **required**

**companyId** string

The company id from which the application is to be uninstalled. If you pass agency token, then companyId is required. It will uninstall application from agency as well as all sub-accounts.

Example:`tDtDnQdgm2LXpyiqYvZ6`

**locationId** string

The location id from which the application is to be uninstalled. If you pass location token, then locationId is required. It will uninstall application from that location only.

Example:`tDtDnQdgm2LXpyiqYvZ6`

**reason** string

The reason for uninstalling the application. Reason is required if you are uninstalling the application as a developer.

Example:`Application is not working as expected`

## Responses

- 200
- 400
- 401
- 422

Successfully uninstalled the application

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

The status of the uninstallation of the application

Example:`true`

```json
{
  "success": true
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
name: Authorizationtype: httpscopes: oauth.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/marketplace/app/:appId/installations' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "companyId": "tDtDnQdgm2LXpyiqYvZ6",
  "locationId": "tDtDnQdgm2LXpyiqYvZ6",
  "reason": "Application is not working as expected"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-Access-OnlyAgency-Access

Bearer Token

Parameters

appId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "companyId": "tDtDnQdgm2LXpyiqYvZ6",
  "locationId": "tDtDnQdgm2LXpyiqYvZ6",
  "reason": "Application is not working as expected"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!