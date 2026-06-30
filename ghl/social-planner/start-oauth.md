---
title: "Start OAuth Flow (Step 1 of 3)"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/start-oauth
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/social-media-posting/oauth/:platform/start
---
# Start OAuth Flow (Step 1 of 3)

```
GET https://services.leadconnectorhq.com/social-media-posting/oauth/:platform/start
```


## OAuth Connection Flow - Step 1: Initiate OAuth

This is the first step in the 3-step OAuth flow to connect a social media account:

1. **Start OAuth** (this endpoint) → User authenticates with the platform
2. **Get Accounts** → Retrieve available pages/channels to connect
3. **Attach Account** → Connect the selected account to your location

### How to Use

Open this API in a browser window (not via cURL) with the required query parameters. The user will be redirected to the platform's OAuth login screen.

### Receiving the OAuth Response

After successful authentication, the OAuth window will post a message back to your application. Listen for this message to get the `accountId` needed for the next step.

```javascript
window.addEventListener('message', function(e) {
  if (e.data && e.data.page === 'social_media_posting') {
    const { actionType, page, platform, placement, accountId, reconnectAccounts } = e.data;
    // Use accountId for Step 2: GET /oauth/{locationId}/{platform}/accounts/{accountId}
  }
}, false);
```

### Event Data Response

| Field | Type | Example | Description |
| --- | --- | --- | --- |
| actionType | string | "close" | The action type |
| page | string | "social-media-posting" | Source page identifier |
| platform | string | "facebook" | The OAuth platform |
| placement | string | "placement" | Placement context |
| accountId | string | "658a9b6833b91e0ecb8f3958" | **Use this for Step 2** |
| reconnectAccounts | string\[\] | \["658a9b...", "efd2da..."\] | Accounts that need reconnection |

### Next Step

Use the `accountId` from the response to call:

```text
GET /social-media-posting/oauth/{locationId}/{platform}/accounts/{accountId}
```

### Platform Notes

- **bluesky**: Currently not supported, will return an error
- **tiktok-business**: Uses a separate business OAuth flow

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

**platform** stringrequired

**Possible values:** \[`google`, `facebook`, `instagram`, `linkedin`, `tiktok`, `tiktok-business`, `youtube`, `pinterest`, `threads`, `bluesky`\]

Social media platform to connect. Each platform has specific account types:

- **google**: Google Business Profile locations
- **facebook**: Facebook Pages
- **instagram**: Instagram Professional Accounts (Business/Creator)
- **linkedin**: LinkedIn Pages and Profiles
- **tiktok**: TikTok Creator Accounts
- **tiktok-business**: TikTok Business Center Accounts
- **youtube**: YouTube Channels
- **pinterest**: Pinterest Business Accounts
- **threads**: Threads Profiles
- **bluesky**: Bluesky Accounts (currently not supported)

Example: facebook

### Query Parameters

**locationId** stringrequired

Location Id

Example: w37swmmLbA02zgqKPpxITe2

**userId** stringrequired

User Id

Example: u37swmmLbA02zgqKPpxITe2

**page** string

Page

Example: integration

**reconnect** string

Reconnect

Example: true

## Responses

- 200
- 400
- 401
- 422

Successful Response

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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/oauth/:platform/start'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

platform — pathrequired

\-\-\-googlefacebookinstagramlinkedintiktoktiktok-businessyoutubepinterestthreadsbluesky

locationId — queryrequired

userId — queryrequired

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

page — query

reconnect — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!