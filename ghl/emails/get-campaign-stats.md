---
title: "Get Campaign Statistics"
source_url: https://marketplace.gohighlevel.com/docs/ghl/emails/get-campaign-stats
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/stats/:source/:sourceId
summary: "Get statistics for email campaigns, workflows, or bulk actions"
---
# Get Campaign Statistics

```
GET https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/stats/:source/:sourceId
```

Get statistics for email campaigns, workflows, or bulk actions

### Requirements

#### Scope(s)

`emails/stats.readonly`

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

Location ID

Example: ve9EPM428h8vShlRW1KT

**source** stringrequired

**Possible values:** \[`email-campaigns`, `workflow-campaigns`, `bulk-actions`\]

Source type: email-campaigns, workflow-campaigns, or bulk-actions

Example: email-campaigns

**sourceId** stringrequired

Source ID of the email campaign, workflow campaign, or bulk action

Example: abc123

### Query Parameters

**subSourceId** string

Workflow action ID. Only valid when source is `workflow-campaigns`

Example: step001

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

**locationId** stringrequired

Location ID

Example:`abc123`

**source** stringrequired

Source type

**Possible values:** \[`email-campaigns`, `workflow-campaigns`, `bulk-actions`\]

Example:`email-campaigns`

**sourceId** stringrequired

Source ID

Example:`campaign123`

**subSourceId** string

Workflow action ID

Example:`step001`

**stats** object

Email performance metrics

**sent** numberrequired

Total emails sent (delivered + accepted + bounced)

Example:`1020`

**accepted** numberrequired

Emails accepted by the mail server

Example:`5`

**delivered** numberrequired

Emails delivered to inbox

Example:`1000`

**opened** numberrequired

Emails opened

Example:`450`

**clicked** numberrequired

Links clicked

Example:`120`

**unsubscribed** numberrequired

Unsubscribes

Example:`5`

**complained** numberrequired

Spam complaints

Example:`2`

**permanentFail** numberrequired

Hard bounces

Example:`15`

**temporaryFail** numberrequired

Soft bounces

Example:`3`

**rejected** numberrequired

Rejected emails

Example:`10`

**failed** numberrequired

Failed emails

Example:`5`

**replied** numberrequired

Replies received

Example:`25`

**openRate** numberrequired

Open rate as percentage of delivered

Example:`45`

**clickRate** numberrequired

Click rate as percentage of delivered

Example:`12`

**unsubscribeRate** numberrequired

Unsubscribe rate as percentage of delivered

Example:`0.5`

**complaintRate** numberrequired

Complaint rate as percentage of delivered

Example:`0.2`

**bounceRate** numberrequired

Bounce rate as percentage of sent

Example:`1.76`

**replyRate** numberrequired

Reply rate as percentage of delivered

Example:`2.5`

**traceId** string

Trace ID of the request

Example:`019e4ef5-a65e-4198-8cf9-8e93dca9bda4`

```json
{
  "locationId": "abc123",
  "source": "email-campaigns",
  "sourceId": "campaign123",
  "subSourceId": "step001",
  "stats": {
    "sent": 1020,
    "accepted": 5,
    "delivered": 1000,
    "opened": 450,
    "clicked": 120,
    "unsubscribed": 5,
    "complained": 2,
    "permanentFail": 15,
    "temporaryFail": 3,
    "rejected": 10,
    "failed": 5,
    "replied": 25,
    "openRate": 45,
    "clickRate": 12,
    "unsubscribeRate": 0.5,
    "complaintRate": 0.2,
    "bounceRate": 1.76,
    "replyRate": 2.5
  },
  "traceId": "019e4ef5-a65e-4198-8cf9-8e93dca9bda4"
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
name: Authorizationtype: httpscopes: emails/stats.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/emails/locations/:locationId/campaigns/stats/:source/:sourceId' \
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

locationId — pathrequired

source — pathrequired

\-\-\-email-campaignsworkflow-campaignsbulk-actions

sourceId — pathrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

subSourceId — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!