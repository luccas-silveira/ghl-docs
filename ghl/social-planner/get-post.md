---
title: "Get post"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/get-post
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/:id
---
# Get post

```
GET https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/:id
```

Get post

## Request

## Responses

- 200
- 400
- 401
- 422

Successful response

Bad Request

Unauthorized

Unprocessable Entity

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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/:id' \
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