---
title: "Appuninstall"
source_url: https://marketplace.gohighlevel.com/docs/webhook/AppUninstall
version: v3
summary: "Called whenever an app is uninstalled"
---
Called whenever an app is uninstalled

#### Schema

```json
{
  "type": "object",
  "properties": {
    "type": {
      "type": "string"
    },
    "appId": {
      "type": "string"
    },
    "companyId": {
      "type": "string"
    },
    "locationId": {
      "type": "string"
    }
  }
}
```

#### Example

- For Location Level App Uninstall

```json
{
  "type": "UNINSTALL",
  "appId": "ve9EPM428h8vShlRW1KT",
  "locationId": "otg8dTQqGLh3Q6iQI55w"
}
```

- For Agency Level App Uninstall

```json
{
  "type": "UNINSTALL",
  "appId": "ve9EPM428h8vShlRW1KT",
  "companyId": "otg8dTQqGLh3Q6iQI55w"
}
```

## Share your feedback

★★★★★