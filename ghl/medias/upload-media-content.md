---
title: "Upload File into Media Storage"
source_url: https://marketplace.gohighlevel.com/docs/ghl/medias/upload-media-content
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/medias/upload-file
---
# Upload File into Media Storage

```
POST https://services.leadconnectorhq.com/medias/upload-file
```


If hosted is set to true then fileUrl is required. Else file is required. If adding a file, maximum allowed is 25 MB. For video files, the maximum allowed size is 500 MB.

### Requirements

#### Scope(s)

`medias.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/medias/upload-media-content/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- multipart/form-data

### Body **required**

**file** binary

**hosted** boolean

**fileUrl** string

**name** string

**parentId** string

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/medias/upload-media-content/\#responses "Direct link to Responses")

- 200

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**fileId** stringrequired

ID of the uploaded file

Example:`file.pdf`

**url** stringrequired

Google Cloud Storage URL of the uploaded file

Example:`https://storage.googleapis.com/bucket-name/path/to/file.pdf`

```json
{
  "fileId": "file.pdf",
  "url": "https://storage.googleapis.com/bucket-name/path/to/file.pdf"
}
```

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
curl -L -X POST 'https://services.leadconnectorhq.com/medias/upload-file' \
-H 'Content-Type: multipart/form-data' \
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

Version — headerrequired

\-\-\-v3

Body required

file

file

hosted

fileUrl

name

parentId

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!