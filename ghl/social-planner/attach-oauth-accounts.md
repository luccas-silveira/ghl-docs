---
title: "Connect Account (Step 3 of 3)"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/oauth/:locationId/:platform/accounts/:accountId
---
# Connect Account (Step 3 of 3)

```
POST https://services.leadconnectorhq.com/social-media-posting/oauth/:locationId/:platform/accounts/:accountId
```

## OAuth Connection Flow - Step 3: Connect the Account [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#oauth-connection-flow---step-3-connect-the-account "Direct link to OAuth Connection Flow - Step 3: Connect the Account")

This is the final step in the OAuth flow. After retrieving available accounts (Step 2), use this endpoint to connect the selected account to your location.

### OAuth Flow Summary [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#oauth-flow-summary "Direct link to OAuth Flow Summary")

1. **Start OAuth** → User authenticates with platform
2. **Get Accounts** → Retrieved available pages/channels
3. **Attach Account** (this endpoint) → Connect the selected account

### Request Body by Platform [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#request-body-by-platform "Direct link to Request Body by Platform")

The request body structure varies depending on the platform:

#### Facebook / Instagram [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#facebook--instagram "Direct link to Facebook / Instagram")

```json
{
  "type": "page",
  "originId": "244405XXXXX11687",
  "name": "My Facebook Page",
  "avatar": "https://..." // optional
}
```

#### Google Business Profile [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#google-business-profile "Direct link to Google Business Profile")

```json
{
  "location": {
    "name": "locations/12345",
    "title": "My Business Location",
    "storeCode": "STORE123",
    "isVerified": "ChIJsZQpj1qbXjkRQNDUG4UUx6k"
  },
  "account": {
    "name": "accounts/12345",
    "accountName": "My Business Account",
    "type": "LOCATION_GROUP",
    "verificationState": "VERIFIED",
    "vettedState": "VETTED"
  }
}
```

#### LinkedIn [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#linkedin "Direct link to LinkedIn")

```json
{
  "type": "page",
  "originId": "urn:li:organization:12345",
  "name": "My LinkedIn Page",
  "avatar": "https://..." // optional
}
```

#### TikTok [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#tiktok "Direct link to TikTok")

```json
{
  "originId": "7234567890123456789",
  "name": "My TikTok Account",
  "avatar": "https://..." // optional
}
```

#### YouTube [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#youtube "Direct link to YouTube")

```json
{
  "originId": "UCxxxxxxxxxxxxxxxx",
  "name": "My YouTube Channel",
  "avatar": "https://..." // optional
}
```

#### Pinterest [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#pinterest "Direct link to Pinterest")

```json
{
  "originId": "123456789",
  "name": "My Pinterest Account",
  "avatar": "https://..." // optional
}
```

### After Connection [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#after-connection "Direct link to After Connection")

Once connected, the account will appear in your location's connected accounts and can be used for social media posting.

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#request "Direct link to Request")

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

The Location ID where you want to connect this social account

Example: w37swmmLbA02zgqKPpxITe2

**platform** stringrequired

**Possible values:** \[`google`, `facebook`, `instagram`, `linkedin`, `tiktok`, `youtube`, `pinterest`, `threads`, `bluesky`\]

Social media platform (must match the platform used in Steps 1 and 2)

Example: facebook

**accountId** stringrequired

The OAuth Account ID received from Step 1 (same as used in Step 2)

Example: w37swmmLbA02zgqKPpxITe

- application/json

### Body **required**

Account details to connect. The structure varies by platform - see description above for examples.

oneOf

- Facebook
- Instagram
- Google Business Account
- Pinterest
- Tiktok
- YouTube
- Linkedin
- Threads

**type** stringrequired

Type of Facebook account (must be page)

**Possible values:** \[`page`\]

Example:`page`

**originId** stringrequired

Original Facebook platform identifier

Example:`244405****11687`

**name** stringrequired

Name of the Facebook page or account

Example:`JOHN_DEO`

**avatar** stringrequired

Avatar or profile picture URL

Example:`https://storage.googleapis.com/2ad21ebc23/test`

**originId** string

Original platform-specific account identifier

Example:`244405****11687`

**name** string

Display name of the account

Example:`JOHN_DEO`

**avatar** string

Avatar or profile picture URL

Example:`https://storage.googleapis.com/2ad21ebc23/test`

**pageId** stringrequired

Facebook page ID associated with the Instagram account

Example:`234234234242sd`

**location** object

**name** stringrequired

Location name

**storeCode** string

Store code

**title** stringrequired

Location title

**storefrontAddress** object

Storefront address details

**metadata** object

Additional metadata

**maxLocation** boolean

Whether this is a max location

**isVerified** boolean

Whether the location is verified

**isConnected** boolean

Whether the location is connected

**account** object

**name** stringrequired

Account name identifier

**accountName** stringrequired

Display name of the account

**type** stringrequired

Type of the account

**verificationState** stringrequired

State of account verification

**vettedState** stringrequired

Vetting state of the account

**originId** stringrequired

Origin ID

Example:`244405****11687`

**name** string

Name

Example:`Ayush`

**avatar** string

Avatar URL

**verified** boolean

Verification status

Example:`true`

**username** string

Username

Example:`@ayush`

**websiteUrl** string

Website URL

Example:`https://www.website.com`

**companyId** string

Company ID

Example:`companyId`

**type** string

Account type must be one of the following values: profile

**Possible values:** \[`profile`\]

**originAccountType** string

Origin account type

**type** stringrequired

Type of TikTok account

**Possible values:** \[`page`, `group`, `profile`, `location`, `business`\]

Example:`profile`

**originId** stringrequired

Original platform-specific account identifier

Example:`244405****11687`

**name** stringrequired

Display name of the account

Example:`JOHN_DEO`

**avatar** stringrequired

Avatar or profile picture URL

Example:`https://example.com/avatar.jpg`

**verified** boolean

Indicates if the TikTok account is verified

Example:`true`

**username** string

Username or handle of the TikTok account

Example:`JOHN_DEO`

**type** stringrequired

Account type

**Possible values:** \[`profile`\]

**originId** stringrequired

Origin ID

Example:`244405****11687`

**name** stringrequired

Name

Example:`Ayush`

**avatar** stringrequired

Avatar URL

**verified** boolean

Verification status

Example:`true`

**username** string

Username

Example:`@ayush`

**type** stringrequired

Type of LinkedIn account (must be one of: page, profile)

**Possible values:** \[`page`, `group`, `profile`, `location`, `business`\]

Example:`page`

**originId** stringrequired

Original LinkedIn platform identifier

Example:`244405****11687`

**name** stringrequired

Name of the LinkedIn page or profile

Example:`JOHN_DEO`

**avatar** stringrequired

Avatar or profile picture URL

Example:`https://storage.googleapis.com/2ad21ebc23/test`

**urn** stringrequired

LinkedIn URN (Uniform Resource Name) identifier

Example:`urn:li:organization:80847980`

**type** stringrequired

Account type

**Possible values:** \[`profile`\]

Example:`profile`

**originId** stringrequired

Origin ID

Example:`244405****11687`

**name** stringrequired

Account name

Example:`JOHN_DEO`

**avatar** stringrequired

Avatar URL

Example:`https://storage.googleapis.com/2ad21ebc23/test`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/attach-oauth-accounts/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Successful response - Account attached. Response structure varies by platform.

- application/json

- Schema
- Example (auto)

**Schema**

oneOf

- Facebook
- Instagram
- Google Business Account
- Linkedin
- Tiktok
- YouTube
- Pinterest

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added Facebook Account`

**results** object

Requested Results

**\_id** string

MongoDB document ID of the social media account

Example:`65f2d989a4f2f1e5322c3856`

**oAuthId** string

OAuth provider account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**oldId** string

Legacy account identifier for backward compatibility

Example:`u37swmmLbA02zgqKPpxITe2`

**locationId** string

Location ID associated with this account

Example:`u37swmmLbA02zgqKPpxITe2`

**originId** string

Original platform-specific account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**platform** object

Social media platform name

Example:`facebook`

**type** object

type value must be page

Example:`page`

**name** string

Display name of the account

Example:`Account Name`

**avatar** string

Avatar or profile picture URL

Example:`u37swmmLbA02zgqKPpxITe2`

**meta** object

Additional metadata for the account

Example:`{"pageId":"u37swmmLbA02zgqKPpxITe2","page":{"id":"u37swmmLbA02zgqKPpxITe2","name":"Account Name","avatar":"u37swmmLbA02zgqKPpxITe2"},"storeCode":"122","isVerified":"true","verified":true,"protected":true,"locationId":"u37swmmLbA02zgqKPpxITe2","accountId":"u37swmmLbA02zgqKPpxITe2","openId":"u37swmmLbA02zgqKPpxITe2","urn":"u37swmmLbA02zgqKPpxITe2","username":"testUser","storefrontAddress":{"regionCode":"30021","languageCode":"E001","postalCode":"1221","administrativeArea":"Down Town","locality":"Louis Street","addressLines":["207","county"]}}`

**active** boolean

Indicates if the account is currently active

Example:`true`

**deleted** boolean

Indicates if the account has been deleted

Example:`true`

**createdAt** date-time

created date

Example:`2024-03-14T11:03:37.015Z`

**updatedAt** date-time

updated date

Example:`2024-03-14T11:03:37.015Z`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added Instagram Account`

**results** object

Requested Results

**\_id** string

MongoDB document ID of the social media account

Example:`65f2d989a4f2f1e5322c3856`

**oAuthId** string

OAuth provider account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**oldId** string

Legacy account identifier for backward compatibility

Example:`u37swmmLbA02zgqKPpxITe2`

**locationId** string

Location ID associated with this account

Example:`u37swmmLbA02zgqKPpxITe2`

**originId** string

Original platform-specific account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**platform** object

Social media platform name

Example:`instagram`

**type** object

Type of account (e.g., location, page, profile)

Example:`profile`

**name** string

Display name of the account

Example:`Profile Name`

**avatar** string

Avatar or profile picture URL

Example:`u37swmmLbA02zgqKPpxITe2`

**meta** object

Additional metadata for the account

Example:`{"pageId":"u37swmmLbA02zgqKPpxITe2","page":{"id":"u37swmmLbA02zgqKPpxITe2","name":"Account Name","avatar":"u37swmmLbA02zgqKPpxITe2"},"storeCode":"122","isVerified":"true","verified":true,"protected":true,"locationId":"u37swmmLbA02zgqKPpxITe2","accountId":"u37swmmLbA02zgqKPpxITe2","openId":"u37swmmLbA02zgqKPpxITe2","urn":"u37swmmLbA02zgqKPpxITe2","username":"testUser","storefrontAddress":{"regionCode":"30021","languageCode":"E001","postalCode":"1221","administrativeArea":"Down Town","locality":"Louis Street","addressLines":["207","county"]}}`

**active** boolean

Indicates if the account is currently active

Example:`true`

**deleted** boolean

Indicates if the account has been deleted

Example:`true`

**createdAt** date-time

created date

Example:`2024-03-14T11:03:37.015Z`

**updatedAt** date-time

updated date

Example:`2024-03-14T11:03:37.015Z`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added Google Business Account`

**results** object

Requested Results

**\_id** string

MongoDB document ID of the social media account

Example:`65f2d989a4f2f1e5322c3856`

**oAuthId** string

OAuth provider account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**oldId** string

Legacy account identifier for backward compatibility

Example:`u37swmmLbA02zgqKPpxITe2`

**locationId** string

Location ID associated with this account

Example:`u37swmmLbA02zgqKPpxITe2`

**originId** string

Original platform-specific account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**platform** object

Social media platform name

Example:`google`

**type** object

Type of account (e.g., location, page, profile)

Example:`location`

**name** string

Display name of the account

Example:`Account Name`

**avatar** string

Avatar or profile picture URL

Example:`u37swmmLbA02zgqKPpxITe2`

**meta** object

Additional metadata for the account

Example:`{"pageId":"u37swmmLbA02zgqKPpxITe2","page":{"id":"u37swmmLbA02zgqKPpxITe2","name":"Account Name","avatar":"u37swmmLbA02zgqKPpxITe2"},"storeCode":"122","isVerified":"true","verified":true,"protected":true,"locationId":"u37swmmLbA02zgqKPpxITe2","accountId":"u37swmmLbA02zgqKPpxITe2","openId":"u37swmmLbA02zgqKPpxITe2","urn":"u37swmmLbA02zgqKPpxITe2","username":"testUser","storefrontAddress":{"regionCode":"30021","languageCode":"E001","postalCode":"1221","administrativeArea":"Down Town","locality":"Louis Street","addressLines":["207","county"]}}`

**active** boolean

Indicates if the account is currently active

Example:`true`

**deleted** boolean

Indicates if the account has been deleted

Example:`true`

**createdAt** date-time

created date

Example:`2024-03-14T11:03:37.015Z`

**updatedAt** date-time

updated date

Example:`2024-03-14T11:03:37.015Z`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Added LinkedIn Account`

**results** object

Requested Results

**\_id** string

MongoDB document ID of the social media account

Example:`65f2d989a4f2f1e5322c3856`

**oAuthId** string

OAuth provider account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**oldId** string

Legacy account identifier for backward compatibility

Example:`u37swmmLbA02zgqKPpxITe2`

**locationId** string

Location ID associated with this account

Example:`u37swmmLbA02zgqKPpxITe2`

**originId** string

Original platform-specific account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**platform** object

Social media platform name

Example:`linkedin`

**type** object

type must be one of the following values: page, profile

Example:`profile`

**name** string

Display name of the account

Example:`Profile Name`

**avatar** string

Avatar or profile picture URL

Example:`u37swmmLbA02zgqKPpxITe2`

**meta** object

Additional metadata for the account

Example:`{"pageId":"u37swmmLbA02zgqKPpxITe2","page":{"id":"u37swmmLbA02zgqKPpxITe2","name":"Account Name","avatar":"u37swmmLbA02zgqKPpxITe2"},"storeCode":"122","isVerified":"true","verified":true,"protected":true,"locationId":"u37swmmLbA02zgqKPpxITe2","accountId":"u37swmmLbA02zgqKPpxITe2","openId":"u37swmmLbA02zgqKPpxITe2","urn":"u37swmmLbA02zgqKPpxITe2","username":"testUser","storefrontAddress":{"regionCode":"30021","languageCode":"E001","postalCode":"1221","administrativeArea":"Down Town","locality":"Louis Street","addressLines":["207","county"]}}`

**active** boolean

Indicates if the account is currently active

Example:`true`

**deleted** boolean

Indicates if the account has been deleted

Example:`true`

**createdAt** date-time

created date

Example:`2024-03-14T11:03:37.015Z`

**updatedAt** date-time

updated date

Example:`2024-03-14T11:03:37.015Z`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added Tiktok Account`

**results** object

Requested Results

**\_id** string

MongoDB document ID of the social media account

Example:`65f2d989a4f2f1e5322c3856`

**oAuthId** string

OAuth provider account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**oldId** string

Legacy account identifier for backward compatibility

Example:`u37swmmLbA02zgqKPpxITe2`

**locationId** string

Location ID associated with this account

Example:`u37swmmLbA02zgqKPpxITe2`

**originId** string

Original platform-specific account identifier

Example:`u37swmmLbA02zgqKPpxITe2`

**platform** object

Social media platform name

Example:`tiktok`

**type** object

type must be one of the following values: profile, business

Example:`profile`

**name** string

Display name of the account

Example:`Account Name`

**avatar** string

Avatar or profile picture URL

Example:`u37swmmLbA02zgqKPpxITe2`

**meta** object

Additional metadata for the account

Example:`{"pageId":"u37swmmLbA02zgqKPpxITe2","page":{"id":"u37swmmLbA02zgqKPpxITe2","name":"Account Name","avatar":"u37swmmLbA02zgqKPpxITe2"},"storeCode":"122","isVerified":"true","verified":true,"protected":true,"locationId":"u37swmmLbA02zgqKPpxITe2","accountId":"u37swmmLbA02zgqKPpxITe2","openId":"u37swmmLbA02zgqKPpxITe2","urn":"u37swmmLbA02zgqKPpxITe2","username":"testUser","storefrontAddress":{"regionCode":"30021","languageCode":"E001","postalCode":"1221","administrativeArea":"Down Town","locality":"Louis Street","addressLines":["207","county"]}}`

**active** boolean

Indicates if the account is currently active

Example:`true`

**deleted** boolean

Indicates if the account has been deleted

Example:`true`

**createdAt** date-time

created date

Example:`2024-03-14T11:03:37.015Z`

**updatedAt** date-time

updated date

Example:`2024-03-14T11:03:37.015Z`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added YouTube Account`

**results** object

Requested Results

**name** stringrequired

Account Name

Example:`John Doe`

**originId** stringrequired

Origin ID

Example:`244405****11687`

**avatar** string

Account Avatar URL

Example:`https://storage.googleapis.com/bucket/avatar.jpg`

**platform** stringrequired

**Possible values:** \[`youtube`\]

Example:`youtube`

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`201`

**message** stringrequired

Message

Example:`Added Pinterest Account`

**results** object

Requested Results

**name** stringrequired

Account Name

Example:`John Doe`

**originId** stringrequired

Origin ID

Example:`244405****11687`

**avatar** string

Account Avatar URL

Example:`https://storage.googleapis.com/bucket/avatar.jpg`

**platform** stringrequired

**Possible values:** \[`pinterest`\]

Example:`pinterest`

```json
{
  "success": true,
  "statusCode": 201,
  "message": "Added Facebook Account",
  "results": {
    "_id": "65f2d989a4f2f1e5322c3856",
    "oAuthId": "u37swmmLbA02zgqKPpxITe2",
    "oldId": "u37swmmLbA02zgqKPpxITe2",
    "locationId": "u37swmmLbA02zgqKPpxITe2",
    "originId": "u37swmmLbA02zgqKPpxITe2",
    "platform": "facebook",
    "type": "page",
    "name": "Account Name",
    "avatar": "u37swmmLbA02zgqKPpxITe2",
    "meta": {
      "pageId": "u37swmmLbA02zgqKPpxITe2",
      "page": {
        "id": "u37swmmLbA02zgqKPpxITe2",
        "name": "Account Name",
        "avatar": "u37swmmLbA02zgqKPpxITe2"
      },
      "storeCode": "122",
      "isVerified": "true",
      "verified": true,
      "protected": true,
      "locationId": "u37swmmLbA02zgqKPpxITe2",
      "accountId": "u37swmmLbA02zgqKPpxITe2",
      "openId": "u37swmmLbA02zgqKPpxITe2",
      "urn": "u37swmmLbA02zgqKPpxITe2",
      "username": "testUser",
      "storefrontAddress": {
        "regionCode": "30021",
        "languageCode": "E001",
        "postalCode": "1221",
        "administrativeArea": "Down Town",
        "locality": "Louis Street",
        "addressLines": [\
          "207",\
          "county"\
        ]
      }
    },
    "active": true,
    "deleted": true,
    "createdAt": "2024-03-14T11:03:37.015Z",
    "updatedAt": "2024-03-14T11:03:37.015Z"
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
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-d '{
  "type": "page",
  "originId": "244405****11687",
  "name": "JOHN_DEO",
  "avatar": "https://storage.googleapis.com/2ad21ebc23/test"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

locationId — pathrequired

platform — pathrequired

\-\-\-googlefacebookinstagramlinkedintiktokyoutubepinterestthreadsbluesky

accountId — pathrequired

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Body required

- Example (from schema)
- facebook
- instagram
- google
- linkedin
- tiktok

```json
{
  "type": "page",
  "originId": "244405****11687",
  "name": "JOHN_DEO",
  "avatar": "https://storage.googleapis.com/2ad21ebc23/test"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!