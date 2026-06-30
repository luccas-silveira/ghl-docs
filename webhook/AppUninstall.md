---
title: "Appuninstall"
source_url: https://marketplace.gohighlevel.com/docs/webhook/AppUninstall
version: v3
---
Called whenever an app is uninstalled

#### Schema [​](https://marketplace.gohighlevel.com/docs/webhook/AppUninstall/\#schema "Direct link to Schema")

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

#### Example [​](https://marketplace.gohighlevel.com/docs/webhook/AppUninstall/\#example "Direct link to Example")

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