---
title: "Get Pipelines"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/get-pipelines
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/opportunities/pipelines
---
# Get Pipelines

```
GET https://services.leadconnectorhq.com/opportunities/pipelines
```


Get Pipelines

### Requirements

#### Scope(s)

`opportunities.readonly`

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

### Query Parameters

**locationId** stringrequired

Identifier of the location (sub-account) to retrieve pipelines for

Example: ve9EPM428h8vShlRW1KT

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**pipelines** object\[\]

List of pipelines for the location

Array \[\
\
**id** string\
\
Unique identifier of the pipeline\
\
Example:`aWdODOBVOlH1RUFKWQke`\
\
**name** string\
\
Name of the pipeline\
\
Example:`new pipeline`\
\
**stages** array\[\]\
\
Stages belonging to this pipeline\
\
Example:`[]`\
\
**showInFunnel** boolean\
\
Whether the pipeline is shown in the funnel view\
\
Example:`false`\
\
**showInPieChart** boolean\
\
Whether the pipeline is shown in the pie chart view\
\
Example:`true`\
\
**locationId** string\
\
Identifier of the location (sub-account) this pipeline belongs to\
\
Example:`dsjddjkndadqaja`\
\
**useOpportunityProbability** boolean\
\
Whether stage-level win probability is enabled for this pipeline\
\
Example:`true`\
\
**colorRenderMode** string\
\
How pipeline/stage colors are rendered\
\
**Possible values:** \[`dot`, `bg-tint`, `none`\]\
\
Example:`dot`\
\
\]

```json
{
  "pipelines": []
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: opportunities.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/opportunities/pipelines' \
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

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!