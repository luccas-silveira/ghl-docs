---
title: "Update an existing knowledge base FAQ"
source_url: https://marketplace.gohighlevel.com/docs/ghl/knowledge-base/update
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/knowledge-bases/faqs/:id
---
# Update an existing knowledge base FAQ

```
PUT https://services.leadconnectorhq.com/knowledge-bases/faqs/:id
```


Update an existing knowledge base FAQ

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Authorization** stringrequired

Access Token

Example: Bearer 9c48df2694a849b6089f9d0d3513efe

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**id** stringrequired

faq ID as string

Example: 710KoEzy793Fxubft0bc

- application/json

### Body **required**

**question** stringrequired

faq question as a string

Example:`What is the capital of France?`

**answer** stringrequired

faq answer as a string

Example:`The capital of France is Paris.`

## Responses

- 200
- 400
- 401
- 422
- 500

FAQ updated successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Success status of the update operation

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

Internal Server Error

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`500`

**message** string

Example:`Internal Server Error`

```json
{
  "statusCode": 500,
  "message": "Internal Server Error"
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
curl -L -X PUT 'https://services.leadconnectorhq.com/knowledge-bases/faqs/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "question": "What is the capital of France?",
  "answer": "The capital of France is Paris."
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

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "question": "What is the capital of France?",
  "answer": "The capital of France is Paris."
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!