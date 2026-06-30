---
title: "Upload file attachments"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversations/upload-file-attachments
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/conversations/messages/upload
summary: "Post the necessary fields for the API to upload files. The files need to be a buffer with the key 'fileAttachment'"
---
# Upload file attachments

```
POST https://services.leadconnectorhq.com/conversations/messages/upload
```


Post the necessary fields for the API to upload files. The files need to be a buffer with the key "fileAttachment".

**Note:** One of conversationId or contactId must be provided.

**File Size Limits:**

- Maximum file size: 5 MB
- Maximum files per upload: 5

**Allowed file types:**

**Images:** JPG, JPEG, PNG, GIF, SVG, HEIC, AI

**Videos:** MP4, MPEG, 3GP

**Audio:** MP3, WAV, WAVE, AIFF, AIF, AIFC, GSM, ULAW, OGG, AAC, M4A, AMR

**Documents:** PDF, DOC, DOCX, TXT, CSV, XLS, XLSX, PPT, PPTX, ODT

**Archives:** ZIP, RAR

**Other:** VCF, VCARD (contact files), ICS (calendar files)

The API will return an object with the URLs

### Requirements

#### Scope(s)

`conversations/message.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- multipart/form-data

### Body **required**

**conversationId** string

Conversation Id

Example:`ve9EPM428h8vShlRW1KT`

**contactId** string

Contact Id

Example:`ve9EPM428h8vShlRW1KT`

**workflowId** string

Workflow Id

Example:`ve9EPM428h8vShlRW1KT`

**campaignId** string

Campaign Id

Example:`ve9EPM428h8vShlRW1KT`

**locationId** stringrequired

**attachmentUrls** string\[\]required

## Responses

- 200
- 400
- 401
- 404
- 413
- 415

Uploaded the file successfully

- application/json

- Schema
- Example (auto)

**Schema**

**uploadedFiles** objectrequired

```json
{
  "uploadedFiles": {}
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

Not Found - Conversation id, contact id, workflow id or campaign id not found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`404`

**message** string

Example:`Conversation id, contact id, workflow id, or campaign id not given`

```json
{
  "statusCode": 404,
  "message": "Conversation id, contact id, workflow id, or campaign id not given"
}
```

Payload Too Large

- application/json

- Schema
- Example (auto)

**Schema**

**status** numberrequired

HTTP Status code of the request

**Possible values:** \[`400`, `404`, `413`, `415`\]

Example:`413`

**message** stringrequired

Error message of the request

Example:`Failed to upload the files`

```json
{
  "status": 413,
  "message": "Failed to upload the files"
}
```

Unsupported Media Type

- application/json

- Schema
- Example (auto)

**Schema**

**status** numberrequired

HTTP Status code of the request

**Possible values:** \[`400`, `404`, `413`, `415`\]

Example:`413`

**message** stringrequired

Error message of the request

Example:`Failed to upload the files`

```json
{
  "status": 413,
  "message": "Failed to upload the files"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: conversations/message.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X POST 'https://services.leadconnectorhq.com/conversations/messages/upload' \
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

conversationId

contactId

workflowId

campaignId

locationIdrequired

attachmentUrlsrequired

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!