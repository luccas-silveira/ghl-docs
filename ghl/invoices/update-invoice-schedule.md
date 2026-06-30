---
title: "Update schedule"
source_url: https://marketplace.gohighlevel.com/docs/ghl/invoices/update-invoice-schedule
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/invoices/schedule/:scheduleId
---
# Update schedule

```
PUT https://services.leadconnectorhq.com/invoices/schedule/:scheduleId
```

API to update an schedule by schedule id

## Request

## Responses

- 200
- 400
- 401
- 422

Successful response

Bad Request

Unauthorized

Unprocessable Entity

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: invoices/schedule.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/invoices/schedule/:scheduleId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
--data-raw '{
  "altId": "6578278e879ad2646715ba9c",
  "altType": "location",
  "name": "string",
  "contactDetails": {
    "id": "6578278e879ad2646715ba9c",
    "name": "Alex",
    "phoneNo": "+1234567890",
    "email": "alex@example.com",
    "additionalEmails": [\
      {\
        "email": "alex@example.com"\
      }\
    ],
    "companyName": "ABC Corp.",
    "address": {
      "addressLine1": "9931 Beechwood",
      "addressLine2": "Beechwood",
      "city": "St. Houston",
      "state": "TX",
      "countryCode": "US",
      "postalCode": "559-6993"
    },
    "customFields": [\
      "string"\
    ]
  },
  "schedule": {
    "executeAt": "string",
    "rrule": {
      "intervalType": "monthly",
      "interval": 2,
      "startDate": "2023-01-01",
      "startTime": "20:45:00",
      "endDate": "2029-11-01",
      "endTime": "18:45:00",
      "dayOfMonth": 15,
      "dayOfWeek": "mo",
      "numOfWeek": -1,
      "monthOfYear": "jan",
      "count": 10,
      "daysBefore": 5,
      "useStartAsPrimaryUserAccepted": true,
      "endType": "by"
    }
  },
  "liveMode": true,
  "businessDetails": {
    "logoUrl": "https://example.com/logo.png",
    "name": "ABC Corp.",
    "phoneNo": "+1-214-559-6993",
    "address": "9931 Beechwood, TX",
    "website": "wwww.example.com",
    "customValues": [\
      "string"\
    ]
  },
  "currency": "string",
  "items": [\
    {\
      "name": "ABC Product",\
      "description": "ABC Corp.",\
      "productId": "6578278e879ad2646715ba9c",\
      "priceId": "6578278e879ad2646715ba9c",\
      "currency": "USD",\
      "amount": 999,\
      "qty": 1,\
      "taxes": [\
        {\
          "_id": "string",\
          "name": "string",\
          "rate": 0,\
          "calculation": "exclusive",\
          "description": "string",\
          "taxId": "string"\
        }\
      ],\
      "automaticTaxCategoryId": "6578278e879ad2646715ba9c",\
      "isSetupFeeItem": true,\
      "type": "one_time",\
      "taxInclusive": true\
    }\
  ],
  "discount": {
    "value": 10,
    "type": "percentage",
    "validOnProductIds": "[ '\''6579751d56f60276e5bd4154'\'' ]"
  },
  "termsNotes": "string",
  "title": "string",
  "attachments": [\
    {\
      "id": "6241712be68f7a98102ba272",\
      "name": "Electronics.pdf",\
      "url": "https://example.com/digital-delivery",\
      "type": "string",\
      "size": 10000\
    }\
  ],
  "miscellaneousCharges": {
    "charges": [\
      [\
        null\
      ]\
    ],
    "collectedMiscellaneousCharges": 10,
    "paidCharges": [\
      {\
        "name": "Processing Fee",\
        "charge": 10,\
        "amount": 10,\
        "_id": "673d01d7d547648a8dab6211"\
      }\
    ]
  }
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-AccessAgency-Access

Bearer Token

Parameters

scheduleId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "altId": "6578278e879ad2646715ba9c",
  "altType": "location",
  "name": "string",
  "contactDetails": {
    "id": "6578278e879ad2646715ba9c",
    "name": "Alex",
    "phoneNo": "+1234567890",
    "email": "alex@example.com",
    "additionalEmails": [\
      {\
        "email": "alex@example.com"\
      }\
    ],
    "companyName": "ABC Corp.",
    "address": {
      "addressLine1": "9931 Beechwood",
      "addressLine2": "Beechwood",
      "city": "St. Houston",
      "state": "TX",
      "countryCode": "US",
      "postalCode": "559-6993"
    },
    "customFields": [\
      "string"\
    ]
  },
  "schedule": {
    "executeAt": "string",
    "rrule": {
      "intervalType": "monthly",
      "interval": 2,
      "startDate": "2023-01-01",
      "startTime": "20:45:00",
      "endDate": "2029-11-01",
      "endTime": "18:45:00",
      "dayOfMonth": 15,
      "dayOfWeek": "mo",
      "numOfWeek": -1,
      "monthOfYear": "jan",
      "count": 10,
      "daysBefore": 5,
      "useStartAsPrimaryUserAccepted": true,
      "endType": "by"
    }
  },
  "liveMode": true,
  "businessDetails": {
    "logoUrl": "https://example.com/logo.png",
    "name": "ABC Corp.",
    "phoneNo": "+1-214-559-6993",
    "address": "9931 Beechwood, TX",
    "website": "wwww.example.com",
    "customValues": [\
      "string"\
    ]
  },
  "currency": "string",
  "items": [\
    {\
      "name": "ABC Product",\
      "description": "ABC Corp.",\
      "productId": "6578278e879ad2646715ba9c",\
      "priceId": "6578278e879ad2646715ba9c",\
      "currency": "USD",\
      "amount": 999,\
      "qty": 1,\
      "taxes": [\
        {\
          "_id": "string",\
          "name": "string",\
          "rate": 0,\
          "calculation": "exclusive",\
          "description": "string",\
          "taxId": "string"\
        }\
      ],\
      "automaticTaxCategoryId": "6578278e879ad2646715ba9c",\
      "isSetupFeeItem": true,\
      "type": "one_time",\
      "taxInclusive": true\
    }\
  ],
  "discount": {
    "value": 10,
    "type": "percentage",
    "validOnProductIds": "[ '6579751d56f60276e5bd4154' ]"
  },
  "termsNotes": "string",
  "title": "string",
  "attachments": [\
    {\
      "id": "6241712be68f7a98102ba272",\
      "name": "Electronics.pdf",\
      "url": "https://example.com/digital-delivery",\
      "type": "string",\
      "size": 10000\
    }\
  ],
  "miscellaneousCharges": {
    "charges": [\
      [\
        null\
      ]\
    ],
    "collectedMiscellaneousCharges": 10,
    "paidCharges": [\
      {\
        "name": "Processing Fee",\
        "charge": 10,\
        "amount": 10,\
        "_id": "673d01d7d547648a8dab6211"\
      }\
    ]
  }
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!