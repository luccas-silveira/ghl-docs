---
title: "Remove Followers"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/remove-followers-opportunity
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/opportunities/:id/followers
---
# Remove Followers

```
DELETE https://services.leadconnectorhq.com/opportunities/:id/followers
```


Allows removal of one or all followers from an opportunity.

### Requirements

#### Scope(s)

`opportunities.write`

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

**id** stringrequired

Opportunity Id

Example: sx6wyHhbFdRXh302Lunr

### Query Parameters

**isRemoveAllFollowers** boolean

Set to true to remove all followers from the opportunity

- application/json

### Body **required**

**followers** string\[\]required

Array of user IDs to add or remove as followers (max 10)

Example:`["sx6wyHhbFdRXh302Lunr","sx6wyHhbFdRXh302Lunr"]`

## Responses

- 200
- 400
- 401
- 422

Followers successfully removed.

- application/json

- Schema
- Example (auto)

**Schema**

**followers** string\[\]

Current list of all follower user IDs after the operation

Example:`["sx6wyHhbFdRXh302Lunr","sx6wyHhbFdRXh302LLss"]`

**followersRemoved** string\[\]

User IDs that were successfully removed as followers

Example:`["Mx6wyHhbFdRXh302Luer","Ka6wyHhbFdRXh302LLsAm"]`

```json
{
  "followers": [\
    "sx6wyHhbFdRXh302Lunr",\
    "sx6wyHhbFdRXh302LLss"\
  ],
  "followersRemoved": [\
    "Mx6wyHhbFdRXh302Luer",\
    "Ka6wyHhbFdRXh302LLsAm"\
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
name: Authorizationtype: httpscopes: opportunities.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/opportunities/:id/followers' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "followers": [\
    "sx6wyHhbFdRXh302Lunr",\
    "sx6wyHhbFdRXh302Lunr"\
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

id — pathrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

isRemoveAllFollowers — query

\-\-\-truefalse

Body required

```json
{
  "followers": [\
    "sx6wyHhbFdRXh302Lunr",\
    "sx6wyHhbFdRXh302Lunr"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!