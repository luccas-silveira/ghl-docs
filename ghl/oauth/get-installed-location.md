---
title: "Get Location where app is installed"
source_url: https://marketplace.gohighlevel.com/docs/ghl/oauth/get-installed-location
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/oauth/installed-locations
summary: "This API allows you fetch location where app is installed upon"
---
# Get Location where app is installed

```
GET https://services.leadconnectorhq.com/oauth/installed-locations
```


This API allows you fetch location where app is installed upon

### Requirements

#### Scope(s)

`oauth.readonly`

#### Auth Method(s)

`OAuth Access Token`

#### Token Type(s)

`Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Query Parameters

**pageSize** number

Max items per page (1-100). Replaces legacy `limit` parameter per AIP-158.

Default value:`20`

Example: 20

**pageToken** string

Opaque token returned in a previous response to fetch the next page. Replaces legacy `skip` parameter per AIP-158.

Example: eyJza2lwIjoyMH0

**query** string

Parameter to search for the installed location by name

Example: location name

**isInstalled** boolean

Filters out location which are installed for specified app under the specified company

Example:

**restrictToUserLocations** boolean

When true, restricts the list to locations the current user has access to (for restricted agency admins and account admins). When false or omitted, no user-based filter is applied for installed list; for backward compatibility, install list (isInstalled=false) is still filtered by user when this param is omitted.

Example:

**companyId** stringrequired

Parameter to search by the companyId

Example: tDtDnQdgm2LXpyiqYvZ6

**appId** stringrequired

Parameter to search by the appId

Example: tDtDnQdgm2LXpyiqYvZ6

**versionId** string

VersionId of the app

Example: tDtDnQdgm2LXpyiqYvZ6

**onTrial** boolean

Filters out locations which are installed for specified app in trial mode

Example:

**planId** string

Filters out location which are installed for specified app under the specified planId

Example:

**locationId** string

locationId

Example: 1245

## Responses

- 200
- 400
- 401
- 404
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**items** object\[\]required

List of locations with their installation status for the requested app

Array \[\
\
**\_id** stringrequired\
\
Location ID\
\
Example:`0IHuJvc2ofPAAA8GzTRi`\
\
**name** stringrequired\
\
Name of the location\
\
Example:`John Deo`\
\
**address** stringrequired\
\
Address linked to location\
\
Example:`47 W 13th St, New York, NY 10011, USA`\
\
**isInstalled** boolean\
\
Check if the requested app is installed for following location\
\
Example:`true`\
\
**versionId** string\
\
Version ID of the installed app version for this location\
\
Example:`6578278e879ad2646715ba9c`\
\
**installedAt** date-time\
\
Timestamp when the app was installed on this location\
\
Example:`2024-01-15T10:30:00.000Z`\
\
\]

**pagination** object

Pagination metadata (AIP-158)

**totalRecords** number

Total number of records matching the query across all pages

Example:`1231`

**hasNextPage** booleanrequired

True when a next page is available

Example:`true`

**hasPrevPage** booleanrequired

True when a previous page is available

Example:`false`

**nextPageToken** string

Opaque token to fetch the next page

Example:`eyJvZmZzZXQiOjIwfQ`

**prevPageToken** string

Opaque token to fetch the previous page

Example:`eyJvZmZzZXQiOjB9`

**currentPageSize** numberrequired

Number of items returned in the current page

Example:`20`

**estimatedTotalRecords** number

Estimated total records; present when exact total is unknown

Example:`1231`

**metadata** object

Query metadata (filters and sort applied)

**filterApplied** object

Filters that were applied to the query

**property name\*** any

Filters that were applied to the query

Example:`{"companyId":"tDtDnQdgm2LXpyiqYvZ6","isInstalled":true}`

**sortApplied** object

Sort order that was applied to the query

**property name\*** any

Sort order that was applied to the query

Example:`{"installedAt":"desc"}`

**installToFutureLocations** boolean

Boolean to control if user wants app to be automatically installed to future locations

Example:`true`

```json
{
  "items": [\
    {\
      "_id": "0IHuJvc2ofPAAA8GzTRi",\
      "name": "John Deo",\
      "address": "47 W 13th St, New York, NY 10011, USA",\
      "isInstalled": true\
    }\
  ],
  "pagination": {
    "totalRecords": 1231,
    "hasNextPage": true,
    "hasPrevPage": false,
    "nextPageToken": "eyJvZmZzZXQiOjIwfQ",
    "prevPageToken": "eyJvZmZzZXQiOjB9",
    "currentPageSize": 20,
    "estimatedTotalRecords": 1231
  },
  "metadata": {
    "filterApplied": {
      "companyId": "tDtDnQdgm2LXpyiqYvZ6",
      "isInstalled": true
    },
    "sortApplied": {
      "installedAt": "desc"
    }
  },
  "installToFutureLocations": true
}
```

Invalid argument (AIP error envelope)

- application/json

- Schema
- Example (auto)

**Schema**

**error** object

AIP-compliant error envelope

**code** stringrequired

Machine-readable error code (see AipErrorCode enum in @platform-core/aip-framework)

Example:`RESOURCE_NOT_FOUND`

**message** stringrequired

Human-readable error message

Example:`The requested App 'abc' was not found.`

**details** object

Additional error context (field name, identifier, etc.)

**property name\*** any

Additional error context (field name, identifier, etc.)

Example:`{"resource":"App","identifier":"abc"}`

**resolution** string

Suggested resolution for the caller

Example:`Verify the App exists and you have permission to access it.`

```json
{
  "error": {
    "code": "RESOURCE_NOT_FOUND",
    "message": "The requested App 'abc' was not found.",
    "details": {
      "resource": "App",
      "identifier": "abc"
    },
    "resolution": "Verify the App exists and you have permission to access it."
  }
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

App not found (AIP error envelope)

- application/json

- Schema
- Example (auto)

**Schema**

**error** object

AIP-compliant error envelope

**code** stringrequired

Machine-readable error code (see AipErrorCode enum in @platform-core/aip-framework)

Example:`RESOURCE_NOT_FOUND`

**message** stringrequired

Human-readable error message

Example:`The requested App 'abc' was not found.`

**details** object

Additional error context (field name, identifier, etc.)

**property name\*** any

Additional error context (field name, identifier, etc.)

Example:`{"resource":"App","identifier":"abc"}`

**resolution** string

Suggested resolution for the caller

Example:`Verify the App exists and you have permission to access it.`

```json
{
  "error": {
    "code": "RESOURCE_NOT_FOUND",
    "message": "The requested App 'abc' was not found.",
    "details": {
      "resource": "App",
      "identifier": "abc"
    },
    "resolution": "Verify the App exists and you have permission to access it."
  }
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
name: Authorizationtype: httpscopes: oauth.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency.
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
curl -L 'https://services.leadconnectorhq.com/oauth/installed-locations' \
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

companyId — queryrequired

appId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

pageSize — query

pageToken — query

query — query

isInstalled — query

\-\-\-truefalse

restrictToUserLocations — query

\-\-\-truefalse

versionId — query

onTrial — query

\-\-\-truefalse

planId — query

locationId — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!