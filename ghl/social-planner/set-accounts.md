---
title: "Set Accounts"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/set-accounts
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/set-accounts
summary: "Set social media accounts for a CSV import to publish posts to"
---
# Set Accounts

```
POST https://services.leadconnectorhq.com/social-media-posting/:locationId/set-accounts
```


Set social media accounts for a CSV import to publish posts to

### Requirements

#### Scope(s)

`socialplanner/csv.write`

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

- application/json

### Body **required**

**accountIds** string\[\]required

Account Ids

Example:`["aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"]`

**filePath** stringrequired

File path

Example:`omaDY3RbWtTP511e/social-import/d23d68c2-82c0-1db6e2.csv`

**rowsCount** numberrequired

Entries Count. rowsCount must be between 1 and number of posts in CSV

Example:`1`

**fileName** stringrequired

Name of file

Example:`test.csv`

**approver** string

Approver User Id

Example:`o6241QsiRwUIJHyjuhos`

**userId** stringrequired

User ID

Example:`ve9EPM428h8vShlRW1KT`

**csvFileType** string

CSV file type - determines the format of the CSV file being imported

**Possible values:** \[`basic`, `advance`\]

Example:`basic`

## Responses

- 201
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

Example:`201`

**message** stringrequired

Message

Example:`Accounts Set Successfully`

**results** object

Requested Results

**csvId** stringrequired

CSV Id

Example:`6953a0be84b7ff10f6025d53`

```json
{
  "success": true,
  "statusCode": 201,
  "message": "Accounts Set Successfully",
  "results": {
    "csvId": "6953a0be84b7ff10f6025d53"
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

Validation error

- application/json

- Schema
- Example (auto)

**Schema**

**status** numberrequired

HTTP Status

Example:`422`

**options** object

Options

Example:`{}`

**message** string\[\]required

Validation error messages

Example:`["accountIds should not be null or undefined","accountIds should not be empty","accountIds must be an array","Invalid account id in accountIds list"]`

**name** stringrequired

Exception name

Example:`UnprocessableEntityException`

**error** stringrequired

Error type

Example:`Unprocessable Entity`

**statusCode** numberrequired

HTTP Status Code

Example:`422`

**traceId** string

Trace ID for debugging

Example:`22b1c520-258a-4473-b378-a97ddfd9d1bc`

```json
{
  "status": 422,
  "options": {},
  "message": [\
    "accountIds should not be null or undefined",\
    "accountIds should not be empty",\
    "accountIds must be an array",\
    "Invalid account id in accountIds list"\
  ],
  "name": "UnprocessableEntityException",
  "error": "Unprocessable Entity",
  "statusCode": 422,
  "traceId": "22b1c520-258a-4473-b378-a97ddfd9d1bc"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: socialplanner/csv.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/:locationId/set-accounts' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "accountIds": [\
    "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
  ],
  "filePath": "omaDY3RbWtTP511e/social-import/d23d68c2-82c0-1db6e2.csv",
  "rowsCount": 1,
  "fileName": "test.csv",
  "approver": "o6241QsiRwUIJHyjuhos",
  "userId": "ve9EPM428h8vShlRW1KT",
  "csvFileType": "basic"
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
  "accountIds": [\
    "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
  ],
  "filePath": "omaDY3RbWtTP511e/social-import/d23d68c2-82c0-1db6e2.csv",
  "rowsCount": 1,
  "fileName": "test.csv",
  "approver": "o6241QsiRwUIJHyjuhos",
  "userId": "ve9EPM428h8vShlRW1KT",
  "csvFileType": "basic"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!