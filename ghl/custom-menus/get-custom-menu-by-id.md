---
title: "Get Custom Menu Link"
source_url: https://marketplace.gohighlevel.com/docs/ghl/custom-menus/get-custom-menu-by-id
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/custom-menus/:customMenuId
summary: "Fetches a single custom menus based on id. This endpoint allows clients to retrieve custom menu configurations, which may include menu items, categories, and associated metadata"
---
# Get Custom Menu Link

```
GET https://services.leadconnectorhq.com/custom-menus/:customMenuId
```


Fetches a single custom menus based on id. This endpoint allows clients to retrieve custom menu configurations, which may include menu items, categories, and associated metadata

### Requirements

#### Scope(s)

`custom-menu-link.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**customMenuId** stringrequired

Unique identifier of the custom menu

Example: 62e589c1-c456-47e1-a9a7-cb8900014311

## Responses

- 200
- 400
- 401
- 403
- 422

Successfully retrieved custom menu. Returns a single custom menu object, potentially including its structure, items, and relevant metadata.

- application/json

- Schema
- Example (auto)

**Schema**

**customMenu** object

Single Custom menu link object

**id** string

Unique identifier for the custom menu

Example:`12345`

**icon** object

Icon information for the menu item

**name** string

Name of the icon

Example:`yin-yang`

**fontFamily** string

Font family of the icon

**Possible values:** \[`fab`, `fas`, `far`\]

**title** string

Title of the custom menu

Example:`Dashboard`

**url** string

URL of the custom menu

Example:`/dashboard`

**order** number

Order of the custom menu

Example:`1`

**showOnCompany** boolean

Filter to show only agency-level menu links. When omitted, fetches both agency and sub-account menu links. Ignored if locationId is provided

Example:`true`

**showOnLocation** boolean

Whether the menu must be displayed for sub-accounts level

Example:`true`

**showToAllLocations** boolean

Whether the menu must be displayed to all sub-accounts

Example:`true`

**locations** string\[\]

List of sub-account IDs where the menu should be shown. This list is applicable only when showOnLocation is true and showToAllLocations is false

Example:`["gfWreTIHL8pDbggBb7af","67WreTIHL8pDbggBb7ty"]`

**openMode** string

Mode for opening the menu link

**Possible values:** \[`iframe`, `new_tab`, `current_tab`\]

**userRole** string

Which user-roles should the menu be accessible to?

**Possible values:** \[`all`, `admin`, `user`\]

**allowCamera** boolean

Indicates if camera access is allowed for this menu

Example:`false`

**allowMicrophone** boolean

Indicates if microphone access is allowed for this menu

Example:`false`

```json
{
  "customMenu": {
    "id": "12345",
    "icon": {
      "name": "yin-yang",
      "fontFamily": "fab"
    },
    "title": "Dashboard",
    "url": "/dashboard",
    "order": 1,
    "showOnCompany": true,
    "showOnLocation": true,
    "showToAllLocations": true,
    "locations": [\
      "gfWreTIHL8pDbggBb7af",\
      "67WreTIHL8pDbggBb7ty"\
    ],
    "openMode": "iframe",
    "userRole": "all",
    "allowCamera": false,
    "allowMicrophone": false
  }
}
```

Bad Request. Invalid query parameters provided.

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

Forbidden. The client does not have necessary permissions to access custom menu.

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
name: Authorizationtype: httpscopes: custom-menu-link.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency (OR) Private Integration Token of Agency.
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
curl -L 'https://services.leadconnectorhq.com/custom-menus/:customMenuId' \
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

customMenuId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!