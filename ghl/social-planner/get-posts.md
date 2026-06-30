---
title: "Get posts"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/get-posts
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/list
summary: "Successful response"
---
# Get posts

```
POST https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/list
```

Get Posts

## Request

## Responses

- 201
- 400
- 401
- 422

Successful response

Bad Request

Unauthorized

Unprocessable Entity

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: socialplanner/post.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/:locationId/posts/list' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "type": "all",
  "accounts": "660a83fc29deacac50033e2b_omaDY3RbWtTP511e808O_17841465964543589, 38bF83fc29deacac50033e2b_omaDY3RbWtr3P11e808O_17841465964543998",
  "skip": "0",
  "limit": "10",
  "fromDate": "2024-01-22T05:32:49.463Z",
  "toDate": "2024-03-20T05:32:49.463Z",
  "includeUsers": "true",
  "postType": "post"
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
  "type": "all",
  "accounts": "660a83fc29deacac50033e2b_omaDY3RbWtTP511e808O_17841465964543589, 38bF83fc29deacac50033e2b_omaDY3RbWtr3P11e808O_17841465964543998",
  "skip": "0",
  "limit": "10",
  "fromDate": "2024-01-22T05:32:49.463Z",
  "toDate": "2024-03-20T05:32:49.463Z",
  "includeUsers": "true",
  "postType": "post"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!