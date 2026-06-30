---
title: "Upsert Opportunity"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/upsert-opportunity
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/opportunities/upsert
---
# Upsert Opportunity

```
POST https://services.leadconnectorhq.com/opportunities/upsert
```


Upsert Opportunity

### Requirements

#### Scope(s)

`opportunities.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/opportunities/upsert-opportunity/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

- application/json

### Body **required**

**id** string

opportunityId

Example:`yWQobCRIhRguQtD2llvk`

**pipelineId** stringrequired

pipeline Id

Example:`bCkKGpDsyPP4peuKowkG`

**locationId** stringrequired

locationId

Example:`CLu7BaljjqrEjBGKTNNe`

**followers** string\[\]required

contactId

Example:`LiKJ2vnRg5ETM8Z19K7`

**isRemoveAllFollowers** booleanrequired

isRemoveAllFollowers

Example:`true`

**followersActionType** stringrequired

followers action type

**Possible values:** \[`add`, `remove`\]

Example:`add`

**name** string

name

Example:`opportunity name`

**status** string

Current status of the opportunity

**Possible values:** \[`open`, `won`, `lost`, `abandoned`, `all`\]

Example:`open`

**pipelineStageId** string

Identifier of the pipeline stage

Example:`7915dedc-8f18-44d5-8bc3-77c04e994a10`

**monetaryValue** object

Monetary value of the opportunity

Example:`220`

**forecastExpectedCloseDate** string

Expected close date. Supported formats: YYYY/MM/DD, MM/DD/YYYY, YYYY-MM-DD, MM-DD-YYYY, YYYY.MM.DD, MM.DD.YYYY, or ISO 8601

Example:`2026-04-23`

**forecastProbability** number

Forecast probability

Example:`20`

**assignedTo** string

Identifier of the user the opportunity is assigned to

Example:`082goXVW3lIExEQPOnd3`

**lostReasonId** string

lost reason Id

Example:`CLu7BaljjqrEjBGKTNNe`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/opportunities/upsert-opportunity/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**opportunity** objectrequired

Updated / New Opportunity

Example:`{}`

**new** booleanrequired

Indicates whether the opportunity was newly created (true) or updated (false)

Example:`true`

```json
{
  "opportunity": {},
  "new": true
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
curl -L 'https://services.leadconnectorhq.com/opportunities/upsert' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "id": "yWQobCRIhRguQtD2llvk",
  "pipelineId": "bCkKGpDsyPP4peuKowkG",
  "locationId": "CLu7BaljjqrEjBGKTNNe",
  "followers": "LiKJ2vnRg5ETM8Z19K7",
  "isRemoveAllFollowers": true,
  "followersActionType": "add",
  "name": "opportunity name",
  "status": "open",
  "pipelineStageId": "7915dedc-8f18-44d5-8bc3-77c04e994a10",
  "monetaryValue": 220,
  "forecastExpectedCloseDate": "2026-04-23",
  "forecastProbability": 20,
  "assignedTo": "082goXVW3lIExEQPOnd3",
  "lostReasonId": "CLu7BaljjqrEjBGKTNNe"
}'
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

```json
{
  "id": "yWQobCRIhRguQtD2llvk",
  "pipelineId": "bCkKGpDsyPP4peuKowkG",
  "locationId": "CLu7BaljjqrEjBGKTNNe",
  "followers": "LiKJ2vnRg5ETM8Z19K7",
  "isRemoveAllFollowers": true,
  "followersActionType": "add",
  "name": "opportunity name",
  "status": "open",
  "pipelineStageId": "7915dedc-8f18-44d5-8bc3-77c04e994a10",
  "monetaryValue": 220,
  "forecastExpectedCloseDate": "2026-04-23",
  "forecastProbability": 20,
  "assignedTo": "082goXVW3lIExEQPOnd3",
  "lostReasonId": "CLu7BaljjqrEjBGKTNNe"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!