---
title: "Notedelete"
source_url: https://marketplace.gohighlevel.com/docs/webhook/NoteDelete
version: v3
---
Called whenever a note is deleted

#### Schema [​](https://marketplace.gohighlevel.com/docs/webhook/NoteDelete/\#schema "Direct link to Schema")

```json
{
  "type": "object",
  "properties": {
    "type": {
      "type": "string"
    },
    "locationId": {
      "type": "string"
    },
    "id": {
      "type": "string"
    },
    "body": {
      "type": "string"
    },
    "contactId": {
      "type": "string"
    },
    "dateAdded": {
      "type": "string"
    }
  }
}
```

#### Example [​](https://marketplace.gohighlevel.com/docs/webhook/NoteDelete/\#example "Direct link to Example")

```json
{
  "type": "NoteDelete",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "id": "otg8dTQqGLh3Q6iQI55w",
  "body": "Loram ipsum",
  "contactId": "CWBf1PR9LvvBkcYqiXlc",
  "dateAdded": "2021-11-26T12:41:02.193Z"
}
```

## Share your feedback

★★★★★