---
title: "Add/Remove Contacts From Business"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/add-remove-contact-from-business
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/contacts/bulk/business
summary: "Add/Remove Contacts From Business . Passing a `null` businessId will remove the businessId from the contacts"
---
# Add/Remove Contacts From Business

```
POST https://services.leadconnectorhq.com/contacts/bulk/business
```


Add/Remove Contacts From Business . Passing a `null` businessId will remove the businessId from the contacts

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

- application/json

### Body **required**

**locationId** stringrequired

Location Id

Example:`PX8m5VwxEbcpFlzYEPVG`

**ids** string\[\]required

List of contact Ids to update (maximum 50)

**Possible values:**`<= 50 characters`

Example:`["IDqvFHGColiyK6jiatuz","pOC0uJ97VYOKH2m3fkMD"]`

**businessId** stringnullablerequired

Business Id to assign to contacts. Pass null to remove business association.

Example:`63b7ec34ea409a9a8bd2a4ff`

## Responses

- 200
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Whether the bulk update was successful

Example:`true`

**ids** string\[\]required

List of contact Ids that were updated

Example:`["pOC0uJ97VYOKH2m3fkMD"]`

```json
{
  "success": true,
  "ids": [\
    "pOC0uJ97VYOKH2m3fkMD"\
  ]
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
curl -L 'https://services.leadconnectorhq.com/contacts/bulk/business' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-d '{
  "locationId": "PX8m5VwxEbcpFlzYEPVG",
  "ids": [\
    "IDqvFHGColiyK6jiatuz",\
    "pOC0uJ97VYOKH2m3fkMD"\
  ],
  "businessId": "63b7ec34ea409a9a8bd2a4ff"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "PX8m5VwxEbcpFlzYEPVG",
  "ids": [\
    "IDqvFHGColiyK6jiatuz",\
    "pOC0uJ97VYOKH2m3fkMD"\
  ],
  "businessId": "63b7ec34ea409a9a8bd2a4ff"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!