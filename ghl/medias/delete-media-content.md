---
title: "Delete File or Folder"
source_url: https://marketplace.gohighlevel.com/docs/ghl/medias/delete-media-content
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/medias/:id
summary: "Deletes specific file or folder from the media storage"
---
# Delete File or Folder

```
DELETE https://services.leadconnectorhq.com/medias/:id
```


Deletes specific file or folder from the media storage

### Requirements

#### Scope(s)

`medias.write`

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

### Query Parameters

**altType** stringrequired

**Possible values:** \[`location`\]

AltType

Example: location

**altId** stringrequired

location Id

## Responses

- 200

Successful response

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: medias.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/medias/:id' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

id — pathrequired

altType — queryrequired

\-\-\-location

altId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!