---
title: "Update Permissions"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/update-location-permissions
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/locations/:locationId/permissions
---
# Update Permissions

```
PUT https://services.leadconnectorhq.com/locations/:locationId/permissions
```


Update Sub-Account (Formerly Location) permissions

### Requirements

#### Scope(s)

`locations/write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/locations/update-location-permissions/\#request "Direct link to Request")

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

**permissions** string\[\]required

Permission plan values to apply for the sub-account

**Possible values:** \[`2-way-text-messaging`, `gmb-messaging`, `web-chat`, `reputation-management`, `facebook-messenger`, `gmb-call-tracking`, `missed-call-text-back`, `text-to-pay`, `calendar`, `crm`, `opportunities`, `email-marketing`, `form-builder`, `survey-builder`, `trigger-links`, `html-builder`, `sms-email-templates`, `funnels`, `websites`, `workflow`, `membership`, `all-reports`, `triggers`, `campaigns`, `launchpad`\]

Example:`["crm","workflow"]`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/locations/update-location-permissions/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**permissions** string\[\]required

Enabled permission names for the sub-account

**Possible values:** \[`2-way-text-messaging`, `gmb-messaging`, `web-chat`, `reputation-management`, `facebook-messenger`, `gmb-call-tracking`, `missed-call-text-back`, `text-to-pay`, `calendar`, `crm`, `opportunities`, `email-marketing`, `form-builder`, `survey-builder`, `trigger-links`, `html-builder`, `sms-email-templates`, `funnels`, `websites`, `workflow`, `membership`, `all-reports`, `triggers`, `campaigns`, `launchpad`\]

Example:`["crm","workflow"]`

```json
{
  "permissions": [\
    "crm",\
    "workflow"\
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
name: Authorizationtype: httpscopes: locations/writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency (OR) Private Integration Token of Agency.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/locations/:locationId/permissions' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "permissions": [\
    "crm",\
    "workflow"\
  ]
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
  "permissions": [\
    "crm",\
    "workflow"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!