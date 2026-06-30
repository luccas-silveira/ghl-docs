---
title: "Locationcreate"
source_url: https://marketplace.gohighlevel.com/docs/webhook/LocationCreate
version: v3
---
Called whenever a location is created.

> Available only to Agency Level Apps.

#### Schema [​](https://marketplace.gohighlevel.com/docs/webhook/LocationCreate/\#schema "Direct link to Schema")

```json
{
  "type": "object",
  "properties": {
    "type": {
      "type": "string"
    },
    "id": {
      "type": "string"
    },
    "name": {
      "type": "string"
    },
    "email": {
      "type": "string"
    },
    "stripeProductId": {
      "type": "string"
    },
    "companyId": {
      "type": "string"
    }
  }
}
```

#### Example [​](https://marketplace.gohighlevel.com/docs/webhook/LocationCreate/\#example "Direct link to Example")

```json
{
  "type": "LocationCreate",
  "id": "ve9EPM428h8vShlRW1KT",
  "companyId": "otg8dTQqGLh3Q6iQI55w",
  "name": "Loram ipsum",
  "email": "mailer@example.com",
  "stripeProductId": "prod_xyz123abc"
}
```

## Share your feedback

★★★★★