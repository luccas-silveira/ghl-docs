---
title: "Update a Brand Board"
source_url: https://marketplace.gohighlevel.com/docs/ghl/brand-boards/update-brand-board
version: v3
method: PATCH
endpoint: https://services.leadconnectorhq.com/brand-boards/:locationId/:id
---
# Update a Brand Board

```
PATCH https://services.leadconnectorhq.com/brand-boards/:locationId/:id
```


Updates an existing Brand Board

### Requirements

#### Scope(s)

`brand-boards/design-kit.write`

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

Location ID where the brand board exists

Example: ve9EPM428h8vShlRW1KT

**id** stringrequired

Brand board ID to update, retrieve, or delete

Example: 507f1f77bcf86cd799439011

- application/json

### Body **required**

**name** string

Name of the brand board

Example:`My Brandboard 2`

**logos** object\[\]

Array of logos for the brand board

Array \[\
\
**id** string\
\
Unique identifier for the logo\
\
Example:`logo_abc123`\
\
**url** stringrequired\
\
Public URL of the logo image. Used for uploading to the brand board folder in media library\
\
Example:`https://storage.googleapis.com/bucket/logos/my-logo.png`\
\
**label** stringrequired\
\
Display label for the logo (e.g., Primary, Secondary)\
\
Example:`Primary Logo`\
\
**path** stringrequired\
\
Storage path of the logo in the media library\
\
Example:`/locations/ve9EPM428h8vShlRW1KT/logos/my-logo.png`\
\
\]

**colors** object\[\]

Array of colors for the brand board

Array \[\
\
**id** string\
\
Unique identifier for the color\
\
Example:`color_xyz789`\
\
**hexa** stringrequired\
\
Color in 8-digit hexadecimal notation with alpha channel\
\
Example:`#FF5733FF`\
\
**rgba** stringrequired\
\
Color with red, green, blue, and alpha channel values\
\
Example:`rgba(255, 87, 51, 1)`\
\
**hex** stringrequired\
\
Color in HEX format\
\
Example:`#FF5733`\
\
**rgb** stringrequired\
\
Color in RGB format\
\
Example:`rgb(255, 87, 51)`\
\
**label** stringrequired\
\
Display label for the color\
\
Example:`Brand Orange`\
\
\]

**fonts** object\[\]

Array of fonts for the brand board

Array \[\
\
**id** string\
\
Unique identifier for the font\
\
Example:`font_def456`\
\
**font** stringrequired\
\
Font family name\
\
Example:`Montserrat`\
\
**fallback** stringrequired\
\
Fallback font family\
\
Example:`sans-serif`\
\
**label** stringrequired\
\
Display label for the font\
\
Example:`Heading Font`\
\
\]

**default** boolean

Set as the default brand board for this location

Example:`true`

**parentId** string

Parent folder ID in media library (reserved for future use)

Example:`507f1f77bcf86cd799439011`

## Responses

- 200
- 400
- 401
- 403
- 404
- 422

Success

- application/json

- Schema
- Example (auto)

**Schema**

**\_id** stringrequired

Brand board ID

Example:`507f1f77bcf86cd799439011`

**locationId** stringrequired

Location ID

Example:`ve9EPM428h8vShlRW1KT`

**name** stringrequired

Brand board name

Example:`My Brand Board`

**logos** object\[\]

Array of logos

Array \[\
\
**id** string\
\
Unique identifier for the logo\
\
Example:`logo_abc123`\
\
**url** stringrequired\
\
Public URL of the logo image. Used for uploading to the brand board folder in media library\
\
Example:`https://storage.googleapis.com/bucket/logos/my-logo.png`\
\
**label** stringrequired\
\
Display label for the logo (e.g., Primary, Secondary)\
\
Example:`Primary Logo`\
\
**path** stringrequired\
\
Storage path of the logo in the media library\
\
Example:`/locations/ve9EPM428h8vShlRW1KT/logos/my-logo.png`\
\
\]

**colors** object\[\]

Array of brand colors

Array \[\
\
**id** string\
\
Unique identifier for the color\
\
Example:`color_xyz789`\
\
**hexa** stringrequired\
\
Color in 8-digit hexadecimal notation with alpha channel\
\
Example:`#FF5733FF`\
\
**rgba** stringrequired\
\
Color with red, green, blue, and alpha channel values\
\
Example:`rgba(255, 87, 51, 1)`\
\
**hex** stringrequired\
\
Color in HEX format\
\
Example:`#FF5733`\
\
**rgb** stringrequired\
\
Color in RGB format\
\
Example:`rgb(255, 87, 51)`\
\
**label** stringrequired\
\
Display label for the color\
\
Example:`Brand Orange`\
\
\]

**fonts** object\[\]

Array of brand fonts

Array \[\
\
**id** string\
\
Unique identifier for the font\
\
Example:`font_def456`\
\
**font** stringrequired\
\
Font family name\
\
Example:`Montserrat`\
\
**fallback** stringrequired\
\
Fallback font family\
\
Example:`sans-serif`\
\
**label** stringrequired\
\
Display label for the font\
\
Example:`Heading Font`\
\
\]

**default** booleanrequired

Whether this is the default brand board for the location

Example:`false`

**deleted** booleanrequired

Whether the brand board has been soft deleted

Example:`false`

**parentId** string

Parent folder ID in media library

Example:`507f1f77bcf86cd799439011`

**folderId** string

Media library folder ID for this brand board

Example:`507f1f77bcf86cd799439011`

**originId** string

Original brand board ID if cloned from snapshot

Example:`507f1f77bcf86cd799439011`

**meta** object

Metadata about the brand board

**updatedBy** string

User ID who last updated the brand board

Example:`user_abc123`

**lastAction** string

Last action performed on the brand board

Example:`UPDATE`

**sourceId** string

Source brand board ID if created from a template

Example:`507f1f77bcf86cd799439011`

**sourceType** string

How the brand board was created

**Possible values:** \[`template`, `blank`, `snapshot`, `url`\]

Example:`blank`

**missingAssets** object

Assets that used fallbacks/defaults (only returned when creating from URL)

**logos** string\[\]required

Logo labels that used fallbacks

Example:`["Footer"]`

**fonts** string\[\]required

Font labels that used defaults

Example:`["Arial"]`

**colors** string\[\]required

Color labels that used defaults

Example:`[]`

**createdAt** string

Creation timestamp

Example:`2024-01-05T12:00:00.000Z`

**updatedAt** string

Last update timestamp

Example:`2024-01-05T12:00:00.000Z`

```json
{
  "_id": "507f1f77bcf86cd799439011",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "name": "My Brand Board",
  "logos": [\
    {\
      "url": "https://storage.googleapis.com/bucket/logos/my-logo.png",\
      "label": "Primary Logo",\
      "path": "/locations/ve9EPM428h8vShlRW1KT/logos/my-logo.png"\
    }\
  ],
  "colors": [\
    {\
      "hexa": "#FF5733FF",\
      "rgba": "rgba(255, 87, 51, 1)",\
      "hex": "#FF5733",\
      "rgb": "rgb(255, 87, 51)",\
      "label": "Brand Orange"\
    }\
  ],
  "fonts": [\
    {\
      "font": "Montserrat",\
      "fallback": "sans-serif",\
      "label": "Heading Font"\
    }\
  ],
  "default": false,
  "deleted": false,
  "parentId": "507f1f77bcf86cd799439011",
  "folderId": "507f1f77bcf86cd799439011",
  "originId": "507f1f77bcf86cd799439011",
  "meta": {
    "updatedBy": "user_abc123",
    "lastAction": "UPDATE",
    "sourceId": "507f1f77bcf86cd799439011",
    "sourceType": "blank"
  },
  "missingAssets": {
    "logos": [\
      "Footer"\
    ],
    "fonts": [\
      "Arial"\
    ],
    "colors": []
  },
  "createdAt": "2024-01-05T12:00:00.000Z",
  "updatedAt": "2024-01-05T12:00:00.000Z"
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

The token does not have access to this location

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

HTTP status code for invalid location access

Example:`403`

**message** string

Error message describing the location access failure

Example:`The token does not have access to this location`

```json
{
  "statusCode": 403,
  "message": "The token does not have access to this location"
}
```

Not Found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

HTTP status code for not found

Example:`404`

**message** string

Error message describing the not found failure

Example:`Not Found`

**error** string

Error type identifier

Example:`The requested resource was not found`

```json
{
  "statusCode": 404,
  "message": "Not Found",
  "error": "The requested resource was not found"
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: brand-boards/design-kit.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PATCH 'https://services.leadconnectorhq.com/brand-boards/:locationId/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "My Brandboard 2",
  "logos": [\
    {\
      "url": "https://storage.googleapis.com/bucket/logos/my-logo.png",\
      "label": "Primary Logo",\
      "path": "/locations/ve9EPM428h8vShlRW1KT/logos/my-logo.png"\
    }\
  ],
  "colors": [\
    {\
      "hexa": "#FF5733FF",\
      "rgba": "rgba(255, 87, 51, 1)",\
      "hex": "#FF5733",\
      "rgb": "rgb(255, 87, 51)",\
      "label": "Brand Orange"\
    }\
  ],
  "fonts": [\
    {\
      "font": "Montserrat",\
      "fallback": "sans-serif",\
      "label": "Heading Font"\
    }\
  ],
  "default": true,
  "parentId": "507f1f77bcf86cd799439011"
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

id — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "name": "My Brandboard 2",
  "logos": [\
    {\
      "url": "https://storage.googleapis.com/bucket/logos/my-logo.png",\
      "label": "Primary Logo",\
      "path": "/locations/ve9EPM428h8vShlRW1KT/logos/my-logo.png"\
    }\
  ],
  "colors": [\
    {\
      "hexa": "#FF5733FF",\
      "rgba": "rgba(255, 87, 51, 1)",\
      "hex": "#FF5733",\
      "rgb": "rgb(255, 87, 51)",\
      "label": "Brand Orange"\
    }\
  ],
  "fonts": [\
    {\
      "font": "Montserrat",\
      "fallback": "sans-serif",\
      "label": "Heading Font"\
    }\
  ],
  "default": true,
  "parentId": "507f1f77bcf86cd799439011"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!