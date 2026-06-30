---
title: "Get Available Accounts (Step 2 of 3)"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/get-oauth-accounts
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/social-media-posting/oauth/:locationId/:platform/accounts/:accountId
---
# Get Available Accounts (Step 2 of 3)

```
GET https://services.leadconnectorhq.com/social-media-posting/oauth/:locationId/:platform/accounts/:accountId
```


## OAuth Connection Flow - Step 2: Get Available Accounts

After completing OAuth authentication (Step 1), use this endpoint to retrieve the list of available pages, channels, or locations that can be connected.

### OAuth Flow Position

1. **Start OAuth** → User authenticates, returns `accountId`
2. **Get Accounts** (this endpoint) → Lists available pages/channels to connect
3. **Attach Account** → Connect the selected account

### What This Returns

The response varies by platform:

| Platform | Returns |
| --- | --- |
| **facebook** | List of Facebook Pages the user manages |
| **instagram** | List of Instagram Professional Accounts (linked to Facebook Pages) |
| **google** | Google Business Profile locations |
| **linkedin** | LinkedIn Pages and Profile |
| **tiktok** | TikTok Creator account info |
| **tiktok-business** | TikTok Business Center accounts |
| **youtube** | YouTube Channels |
| **pinterest** | Pinterest Business accounts and boards |
| **threads** | Threads profiles |

### Next Step

From the response, select the account/page you want to connect and use its details in Step 3:

```text
POST /social-media-posting/oauth/{locationId}/{platform}/accounts/{accountId}
```

## Request

### Header Parameters

**Authorization** stringrequired

Access Token

Example: Bearer 9c48df2694a849b6089f9d0d3513efe

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**locationId** stringrequired

Account Location Id

Example: w37swmmLbA02zgqKPpxITe2

**platform** stringrequired

**Possible values:** \[`google`, `facebook`, `instagram`, `linkedin`, `tiktok`, `tiktok-business`, `youtube`, `pinterest`, `threads`, `bluesky`\]

Social media platform

Example: facebook

**accountId** stringrequired

The OAuth Account ID received from Step 1 (Start OAuth) via the window message event

Example: w37swmmLbA02zgqKPpxITe

### Query Parameters

**search** string

Search term to filter accounts/pages by name. Useful when the user has many pages to choose from.

Example: My Business Page

## Responses

- 200
- 400
- 401
- 422

Returns available accounts/pages/channels that can be connected. Response structure varies by platform - see examples below.

- application/json

- Schema
- Example (auto)
- facebook
- instagram
- google
- linkedin
- tiktok
- youtube
- pinterest

**Schema**

oneOf

- Facebook
- Instagram
- Google Business Account
- Linkedin
- Tiktok
- Tiktok Business
- YouTube
- Pinterest

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Facebook Account`

**results** object

Requested Results

**pages** object\[\]

Facebook Pages Details

Array \[\
\
**id** string\
\
Facebook page identifier\
\
Example:`u37swmmLbA02zgqKPpxITe2`\
\
**name** string\
\
Name of the Facebook page\
\
Example:`FB Page`\
\
**avatar** string\
\
Avatar or profile picture URL of the page\
\
Example:`u37swmmLbA02zgqKPpxITe2`\
\
**isOwned** boolean\
\
Indicates if the user owns this page\
\
Example:`true`\
\
**isConnected** boolean\
\
Indicates if the page is currently connected\
\
Example:`true`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Instagram Account`

**results** object

Requested Results

**accounts** object\[\]

Instagram Account Details

Array \[\
\
**id** string\
\
Instagram account identifier\
\
Example:`idu37swmmLbA02zgqKPpxITe2`\
\
**name** string\
\
Display name of the Instagram account\
\
Example:`Insta account`\
\
**avatar** string\
\
Avatar or profile picture URL\
\
Example:`avau37swmmLbA02zgqKPpxITe2`\
\
**pageId** string\
\
Facebook page ID associated with the Instagram account\
\
Example:`pidu37swmmLbA02zgqKPpxITe2`\
\
**isConnected** boolean\
\
Indicates if the account is currently connected\
\
Example:`true`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Google Business Account`

**results** object

Requested Results

**locations** object

Locations

**location** object

Google Location Details

**name** string

Google Business account identifier

Example:`accounts/114659701071209971352`

**storeCode** string

Store code or location identifier

Example:`w37swmmLbA02zgqKPpxITe`

**title** string

Business location title or name

Example:`Location Title`

**metadata** object

Meta data not related to User

Example:`{}`

**storefrontAddress** object

Store front address

Example:`{}`

**relationshipData** object

All locations and chain related to this one

Example:`{}`

**maxLocation** boolean

Indicates if location limit has been reached

Example:`true`

**isVerified** boolean

Indicates if the location is verified by Google

Example:`true`

**isConnected** boolean

Indicates if the location is currently connected

Example:`true`

**account** object

Google Account Details

**name** string

Google Business account identifier

Example:`accounts/114659701071209971352`

**accountName** string

Display name of the Google Business account

Example:`Account Name Test`

**type** string

Type of Google Business account

Example:`PERSONAL`

**verificationState** string

Verification state of the account

Example:`UNVERIFIED`

**vettedState** string

Vetted state of the account by Google

Example:`NOT_VETTED`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched LinkedIn Account`

**results** object

Requested Results

**pages** object\[\]

LinkedIn Pages

Array \[\
\
**id** string\
\
Page ID\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
LinkedIn Page Name\
\
Example:`Sample Name`\
\
**avatar** string\
\
Profile Avatar url\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**urn** string\
\
URN\
\
Example:`urn:li:organization:80847980`\
\
**isConnected** boolean\
\
is connected to app\
\
Example:`true`\
\
\]

**profile** object\[\]

LinkedIn Profile Details

Array \[\
\
**id** string\
\
Id\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
Name of profile\
\
Example:`Profile Name`\
\
**avatar** string\
\
Profile avatar\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**urn** string\
\
URN\
\
Example:`urn:li:person:ABC123XYZ`\
\
**isConnected** boolean\
\
is connected to app\
\
Example:`true`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Tiktok Account`

**results** object

Requested Results

**profile** object\[\]

Tiktok Business Account

Array \[\
\
**id** string\
\
Id\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
Name of account\
\
Example:`Account Name`\
\
**username** string\
\
Username of account\
\
Example:`User_name`\
\
**avatar** string\
\
Avatar of profile account\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**verified** boolean\
\
Is verified\
\
Example:`true`\
\
**isConnected** boolean\
\
Is connected\
\
Example:`true`\
\
**type** object\
\
Tiktok Account Type must be one of the following values: business, profile\
\
Example:`BUSINESS`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Fetched Tiktok Business Account`

**results** object

Requested Results

**profile** object\[\]

Tiktok Profile

Array \[\
\
**id** string\
\
Id\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
Name of account\
\
Example:`Account Name`\
\
**username** string\
\
Username of account\
\
Example:`User_name`\
\
**avatar** string\
\
Avatar of profile account\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**verified** boolean\
\
Is verified\
\
Example:`true`\
\
**isConnected** boolean\
\
Is connected\
\
Example:`true`\
\
**type** object\
\
Tiktok Account Type must be one of the following values: business, profile\
\
Example:`BUSINESS`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched YouTube Account`

**results** object

Requested Results

**profile** object\[\]

Youtube Profile

Array \[\
\
**id** string\
\
Id\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
Name of account\
\
Example:`Account Name`\
\
**username** string\
\
Username of account\
\
Example:`@username`\
\
**avatar** string\
\
Avatar of profile account\
\
Example:`https://yt3.ggpht.com/example-avatar`\
\
**verified** boolean\
\
Is verified\
\
Example:`true`\
\
**isConnected** boolean\
\
Is connected\
\
Example:`true`\
\
**type** string\
\
Youtube Account Type\
\
Example:`PROFILE`\
\
\]

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Pinterest Account`

**results** object

Requested Results

**profile** object\[\]

Pinterest Profile

Array \[\
\
**id** string\
\
Id\
\
Example:`w37swmmLbA02zgqKPpxITe`\
\
**name** string\
\
Name of account\
\
Example:`Account Name`\
\
**username** string\
\
Username of account\
\
Example:`@username`\
\
**avatar** string\
\
Avatar of profile account\
\
Example:`https://i.pinimg.com/example-avatar.jpg`\
\
**isConnected** boolean\
\
Is connected\
\
Example:`true`\
\
**type** string\
\
Pinterest Account Type\
\
Example:`PINNER`\
\
**websiteUrl** string\
\
Pinterest Account website Url\
\
Example:`https://www.pinterest.com/`\
\
\]

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Facebook Account",
  "results": {
    "pages": [\
      {\
        "id": "u37swmmLbA02zgqKPpxITe2",\
        "name": "FB Page",\
        "avatar": "u37swmmLbA02zgqKPpxITe2",\
        "isOwned": true,\
        "isConnected": true\
      }\
    ]
  }
}
```

Facebook Pages Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Facebook Account",
  "results": {
    "pages": [\
      {\
        "id": "244405123411687",\
        "name": "My Business Page",\
        "avatar": "https://graph.facebook.com/244405123411687/picture",\
        "isOwned": true,\
        "isConnected": false\
      },\
      {\
        "id": "567890123456789",\
        "name": "Another Page",\
        "avatar": "https://graph.facebook.com/567890123456789/picture",\
        "isOwned": false,\
        "isConnected": true\
      }\
    ]
  }
}
```

Instagram Professional Accounts Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Instagram Account",
  "results": {
    "accounts": [\
      {\
        "id": "17841405123456789",\
        "name": "my_instagram_business",\
        "avatar": "https://...",\
        "isConnected": false,\
        "pageId": "244405123411687",\
        "isBusinessAccount": true\
      }\
    ]
  }
}
```

Google Business Profile Locations Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Google Business Account",
  "results": {
    "locations": {
      "location": {
        "name": "locations/12345678901234567890",
        "storeCode": "STORE001",
        "title": "My Business Location",
        "metadata": {
          "hasGoogleUpdated": true,
          "canDelete": true
        },
        "storefrontAddress": {
          "locality": "New York",
          "regionCode": "US"
        },
        "isVerified": true,
        "isConnected": false
      },
      "account": {
        "name": "accounts/123456789012345678",
        "accountName": "My Business Account",
        "type": "PERSONAL",
        "verificationState": "VERIFIED",
        "vettedState": "VETTED"
      }
    }
  }
}
```

LinkedIn Pages & Profile Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched LinkedIn Account",
  "results": {
    "pages": [\
      {\
        "id": "urn:li:organization:12345678",\
        "name": "My Company",\
        "avatar": "https://...",\
        "isConnected": false\
      }\
    ],
    "profile": {
      "id": "urn:li:person:AbCdEfGhIj",
      "name": "John Doe",
      "avatar": "https://..."
    }
  }
}
```

TikTok Creator Account Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched TikTok Account",
  "results": {
    "openId": "7234567890123456789",
    "displayName": "My TikTok",
    "avatarUrl": "https://...",
    "isConnected": false
  }
}
```

YouTube Channels Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched YouTube Account",
  "results": {
    "channels": [\
      {\
        "id": "UCabcdefghijklmnop",\
        "name": "My YouTube Channel",\
        "avatar": "https://...",\
        "isConnected": false\
      }\
    ]
  }
}
```

Pinterest Account Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Pinterest Account",
  "results": {
    "id": "123456789012345678",
    "username": "mybusiness",
    "businessName": "My Pinterest Business",
    "avatar": "https://...",
    "isConnected": false
  }
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

## Share your feedback

★★★★★

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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/oauth/:locationId/:platform/accounts/:accountId' \
-H 'Accept: application/json'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

locationId — pathrequired

platform — pathrequired

\-\-\-googlefacebookinstagramlinkedintiktoktiktok-businessyoutubepinterestthreadsbluesky

accountId — pathrequired

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

search — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!