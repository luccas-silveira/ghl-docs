---
title: "Get Conversation Channel"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/get-conversation-channel
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/locations/:locationId/conversationChannels/:type
summary: "Get the conversation channel providers configured for a location by type (SMS or Email)"
---
# Get Conversation Channel

```
GET https://services.leadconnectorhq.com/locations/:locationId/conversationChannels/:type
```


Get the conversation channel providers configured for a location by type (SMS or Email)

### Requirements

#### Scope(s)

`locations.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

**type** stringrequired

**Possible values:** \[`SMS`, `Email`\]

Channel type to retrieve providers for

## Responses

- 200
- 400
- 401
- 422

Retrieved all the conversation channels

- application/json

- Schema
- Example (auto)

**Schema**

**conversationChannel** objectrequired

**SMS** object\[\]

List of SMS providers configured for this location

Array \[\
\
**conversationProvider** objectrequired\
\
**\_id** stringrequired\
\
Provider ID\
\
Example:`twilio_provider`\
\
**name** stringrequired\
\
Provider name\
\
Example:`Twilio`\
\
**type** stringrequired\
\
Provider type\
\
**Possible values:** \[`SMS`, `Email`\]\
\
Example:`SMS`\
\
**default** booleanrequired\
\
Whether this is the default provider\
\
Example:`true`\
\
\]

**Email** object\[\]

List of Email providers configured for this location

Array \[\
\
**conversationProvider** objectrequired\
\
**\_id** stringrequired\
\
Provider ID\
\
Example:`twilio_provider`\
\
**name** stringrequired\
\
Provider name\
\
Example:`Twilio`\
\
**type** stringrequired\
\
Provider type\
\
**Possible values:** \[`SMS`, `Email`\]\
\
Example:`SMS`\
\
**default** booleanrequired\
\
Whether this is the default provider\
\
Example:`true`\
\
\]

```json
{
  "conversationChannel": {
    "SMS": [\
      {\
        "conversationProvider": {\
          "_id": "twilio_provider",\
          "name": "Twilio",\
          "type": "SMS",\
          "default": true\
        }\
      }\
    ],
    "Email": [\
      {\
        "conversationProvider": {\
          "_id": "twilio_provider",\
          "name": "Twilio",\
          "type": "SMS",\
          "default": true\
        }\
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
name: Authorizationtype: httpscopes: locations.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/locations/:locationId/conversationChannels/:type' \
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

type — pathrequired

\-\-\-SMSEmail

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!