---
title: "Update File/ Folder"
source_url: https://marketplace.gohighlevel.com/docs/ghl/medias/update-media-object
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/medias/:id
summary: "Updates a single file or folder by ID"
---
# Update File/ Folder

```
POST https://services.leadconnectorhq.com/medias/:id
```


Updates a single file or folder by ID

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

### Path Parameters

**id** stringrequired

Unique identifier of the file or folder to update

Example: 686f9817f0d3165be9fbcef6

- application/json

### Body **required**

**name** stringrequired

New name for the file or folder

Example:`Updated File Name.pdf`

**altType** stringrequired

Type of entity that owns the file or folder

**Possible values:** \[`location`\]

Example:`location`

**altId** stringrequired

Location identifier that owns the file or folder

Example:`sx6wyHhbFdRXh302LLNR`

## Responses

- 200

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

```json
{
  "updated": true,
  "traceId": "33a641a2-c4a6-4123-aa82-c5b84f1a14ee"
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
curl -L 'https://services.leadconnectorhq.com/medias/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "Updated File Name.pdf",
  "altType": "location",
  "altId": "sx6wyHhbFdRXh302LLNR"
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

Body required

```json
{
  "name": "Updated File Name.pdf",
  "altType": "location",
  "altId": "sx6wyHhbFdRXh302LLNR"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!