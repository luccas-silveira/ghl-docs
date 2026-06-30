---
title: "Search Opportunity"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/search-opportunity
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/opportunities/search
summary: "Search Opportunity"
---
# Search Opportunity

```
GET https://services.leadconnectorhq.com/opportunities/search
```


Search Opportunity

### Requirements

#### Scope(s)

`opportunities.readonly`

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

### Query Parameters

**q** string

Search query (max 75 characters)

Example: john@deo.com

**status** string

**Possible values:** \[`open`, `won`, `lost`, `abandoned`, `all`\]

Filter by opportunity status

Example: open

**campaignId** string

Campaign Id

Example: Y2I9XM7aO1hncuSOlc9L

**id** string

Opportunity Id

Example: 123akv4LFn6C9frZoy3e

**order** string

Sort order for results (e.g. added\_asc, added\_desc, name\_asc, name\_desc)

Example: added\_asc

**endDate** string

End date

Example: mm-dd-yyyy

**startAfter** string

Start After

Example: 1628008053263

**startAfterId** string

Start After Id

Example: UIaE1WjAwWKdlyD7osQI

**date** string

Start date

Example: mm-dd-yyyy

**country** string

Filter by country code (ISO 3166-1 alpha-2)

Example: US

**page** number

Page number for pagination

Default value:`1`

Example: 1

**limit** number

Limit Per Page records count. will allow maximum up to 100 and default will be 20

Default value:`20`

Example: 20

**getTasks** boolean

get Tasks in contact

**getNotes** boolean

get Notes in contact

**getCalendarEvents** boolean

get Calender event in contact

**locationId** stringrequired

Location Id

Example: i2SpAtBVHSVea1sL6oah

**pipelineId** string

Pipeline Id

Example: bCkKGpDsyPP4peuKowkG

**pipelineStageId** string

Stage Id

Example: 7915dedc-8f18-44d5-8bc3-77c04e994a10

**contactId** string

Contact Id

Example: WFwVrSSjZ2CNHbZThQX2

**assignedTo** string

Filter by assigned user identifier

Example: 082goXVW3lIExEQPOnd3

## Responses

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**opportunities** object\[\]

List of opportunities matching the search criteria

Array \[\
\
**id** string\
\
Unique identifier of the opportunity\
\
Example:`yWQobCRIhRguQtD2llvk`\
\
**name** string\
\
Name of the opportunity\
\
Example:`testing`\
\
**monetaryValue** number\
\
Monetary value of the opportunity\
\
Example:`500`\
\
**pipelineId** string\
\
Identifier of the pipeline the opportunity belongs to\
\
Example:`VDm7RPYC2GLUvdpKmBfC`\
\
**pipelineStageId** string\
\
Identifier of the pipeline stage the opportunity is in\
\
Example:`e93ba61a-53b3-45e7-985a-c7732dbcdb69`\
\
**assignedTo** string\
\
Identifier of the user the opportunity is assigned to\
\
Example:`zT46WSCPbudrq4zhWMk6`\
\
**status** string\
\
Current status of the opportunity\
\
Example:`open`\
\
**source** string\
\
Source of the opportunity\
\
Example:``\
\
**lastStatusChangeAt** string\
\
ISO 8601 timestamp of the last status change\
\
Example:`2021-08-03T04:55:17.355Z`\
\
**lastStageChangeAt** string\
\
ISO 8601 timestamp of the last stage change\
\
Example:`2021-08-03T04:55:17.355Z`\
\
**lastActionDate** string\
\
ISO 8601 timestamp of the last action on the opportunity\
\
Example:`2021-08-03T04:55:17.355Z`\
\
**indexVersion** string\
\
Index version of the opportunity record\
\
Example:`1`\
\
**createdAt** string\
\
ISO 8601 timestamp when the opportunity was created\
\
Example:`2021-08-03T04:55:17.355Z`\
\
**updatedAt** string\
\
ISO 8601 timestamp when the opportunity was last updated\
\
Example:`2021-08-03T04:55:17.355Z`\
\
**forecastExpectedCloseDate** string\
\
Expected close date for the forecast (YYYY-MM-DD)\
\
Example:`2026-05-20`\
\
**forecastOriginalCloseDate** string\
\
Original forecast close date before any slippage (YYYY-MM-DD)\
\
Example:`2026-05-01`\
\
**forecastSlippageCount** number\
\
Number of times the close date has slipped\
\
Example:`2`\
\
**forecastDaysSlipped** number\
\
Total days the close date has slipped\
\
Example:`19`\
\
**forecastLastSlippedAt** string\
\
ISO 8601 timestamp of the last close-date slip\
\
Example:`2026-05-22T10:30:00.000Z`\
\
**forecastProbability** number\
\
Forecast win probability percentage (0–100)\
\
Example:`20`\
\
**effectiveProbability** number\
\
Effective win probability after stage and forecast adjustments (0–100)\
\
Example:`40`\
\
**contactId** string\
\
Identifier of the contact linked to the opportunity\
\
Example:`zT46WSCPbudrq4zhWMk6`\
\
**locationId** string\
\
Identifier of the location (sub-account) the opportunity belongs to\
\
Example:`zT46WSCPbudrq4zhW`\
\
**contact** object\
\
Contact details associated with the opportunity\
\
**id** string\
\
Unique identifier of the contact\
\
Example:`byMEV0NQinDhq8ZfiOi2`\
\
**name** string\
\
Full name of the contact\
\
Example:`John Deo`\
\
**companyName** string\
\
Company name associated with the contact\
\
Example:`Tesla Inc`\
\
**email** string\
\
Email address of the contact\
\
Example:`john@deo.com`\
\
**phone** string\
\
Phone number of the contact\
\
Example:`+1202-555-0107`\
\
**tags** string\[\]\
\
Tags associated with the contact\
\
Example:`["lead","vip"]`\
\
**notes** array\[\]\
\
Notes attached to the opportunity\
\
Example:`[]`\
\
**tasks** array\[\]\
\
Tasks attached to the opportunity\
\
Example:`[]`\
\
**calendarEvents** array\[\]\
\
Calendar events attached to the opportunity\
\
Example:`[]`\
\
**lostReasonId** string\
\
Identifier of the lost reason if the opportunity was marked lost\
\
Example:`zT46WSCPbudrq4zhWMk6`\
\
**customFields** object\[\]\
\
Custom fields associated with the opportunity\
\
Array \[\
\
**id** stringrequired\
\
Unique identifier of the custom field\
\
Example:`MgobCB14YMVKuE4Ka8p1`\
\
**fieldValue** objectrequired\
\
The value of the custom field\
\
oneOf\
\
- MOD1\
- MOD2\
- MOD3\
- MOD4\
\
string\
\
object\
\
Array \[\
\
string\
\
\]\
\
Array \[\
\
object\
\
\]\
\
\]\
\
**followers** array\[\]\
\
User IDs following this opportunity\
\
Example:`["sx6wyHhbFdRXh302Lunr"]`\
\
**externalObjectId** string\
\
External object identifier for integrations\
\
Example:`ext_obj_12345`\
\
\]

**meta** object

Pagination metadata for the result set

**total** number

Total number of opportunities matching the query

Example:`1`

**nextPageUrl** string

URL to retrieve the next page of results

Example:`http://localhost:5066/opportunities/search?q=&location_id=ve9EPM428h8vShlRW1KT&pipeline_id=&pipeline_stage_id=&status=&assigned_to+=&campaignId=&id=&order=&endDate=&startAfter=1625203104328&startAfterId=yWQobCRIhRguQtD2llvk&date=&limit=1&country=&page=1`

**startAfterId** string

Cursor id to use for pagination (startAfterId param)

Example:`yWQobCRIhRguQtD2llvk`

**startAfter** number

Cursor timestamp to use for pagination (startAfter param)

Example:`1625203104328`

**currentPage** number

Current page number

Example:`2`

**nextPage** number

Next page number

Example:`3`

**prevPage** number

Previous page number

Example:`1`

**aggregations** object

Aggregation results keyed by aggregation name

Example:`{}`

```json
{
  "opportunities": [],
  "meta": {},
  "aggregations": {}
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

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: opportunities.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/opportunities/search' \
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

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

q — query

status — query

\-\-\-openwonlostabandonedall

campaignId — query

id — query

order — query

endDate — query

startAfter — query

startAfterId — query

date — query

country — query

page — query

limit — query

getTasks — query

\-\-\-truefalse

getNotes — query

\-\-\-truefalse

getCalendarEvents — query

\-\-\-truefalse

pipelineId — query

pipelineStageId — query

contactId — query

assignedTo — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!