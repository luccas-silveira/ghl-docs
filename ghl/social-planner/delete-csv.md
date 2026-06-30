---
title: "Delete CSV"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/delete-csv
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id
summary: "Delete a CSV import and all its associated posts"
---
# Delete CSV

```
DELETE https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id
```


Delete a CSV import and all its associated posts

### Requirements

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

**id** stringrequired

CSV Id

Example: 65f92e55cc884f0d0845e447

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

Example:`Deleted CSV`

**results** object

Requested Results

**csv** object

CSV Data

**locationId** string

Location Id

Example:`ve9EPM428h8vShlRW1KT`

**fileName** string

Name of the CSV file

Example:`sample.csv`

**accountIds** string\[\]

Account Ids

Example:`["aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"]`

**file** string

File path of the CSV

Example:`omaDY3RbWtTP511e/social-import/d23d68c2-82c0-1db6e2.csv`

**status** string

CSV import status

**Possible values:** \[`pending`, `in_progress`, `completed`, `failed`, `in_review`, `importing`, `deleted`\]

Example:`completed`

**count** number

Number of posts in the CSV

Example:`5`

**createdBy** string

User Id who created the CSV import

Example:`AccountId_SDsdfdf45Dgs4w3ssss`

**traceId** string

Trace Id for debugging

Example:`FSeSDsdfdf45Dgs4w3ssss`

**originId** string

Origin Id for tracking source

Example:`FSeSDsdfdf45Dgs4w3ssss`

**approver** string

Approver User Id

Example:`FSeSDsdfdf45Dgs4w3ssss`

**csvFileType** string

CSV file type

**Possible values:** \[`basic`, `advance`\]

Example:`basic`

**mediaOptimization** boolean

Media optimization flag

Example:`true`

**applyWatermark** boolean

Apply watermark flag

Example:`false`

**updatedAt** date-time

Date Updated

Example:`2023-08-02T00:00:00.000Z`

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Deleted CSV",
  "results": {
    "csv": {
      "locationId": "ve9EPM428h8vShlRW1KT",
      "fileName": "sample.csv",
      "status": "deleted",
      "count": 5
    }
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
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id' \
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

id — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!