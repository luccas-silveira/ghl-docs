---
title: "Search Contacts"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/search-contacts-advanced
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/contacts/search
---
# Search Contacts

```
POST https://services.leadconnectorhq.com/contacts/search
```


Search contacts based on combinations of advanced filters. Documentation Link - [https://doc.clickup.com/8631005/d/h/87cpx-158396/6e629989abe7fad](https://doc.clickup.com/8631005/d/h/87cpx-158396/6e629989abe7fad)

### Requirements

#### Scope(s)

`contacts.readonly`

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

- application/json

### Body **required**

object

## Responses

- 200
- 400
- 401

Success

Bad Request

Unauthorized

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: contacts.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/contacts/search' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{}'
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

```json
{}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!