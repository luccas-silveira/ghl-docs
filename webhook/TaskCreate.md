---
title: "Taskcreate"
source_url: https://marketplace.gohighlevel.com/docs/webhook/TaskCreate
version: v3
---
Called whenever a task is created

#### Schema [​](https://marketplace.gohighlevel.com/docs/webhook/TaskCreate/\#schema "Direct link to Schema")

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
    "assignedTo": {
      "type": "string"
    },
    "body": {
      "type": "string"
    },
    "contactId": {
      "type": "string"
    },
    "title": {
      "type": "string"
    },
    "dateAdded": {
      "type": "string"
    },
    "dueDate": {
      "type": "string"
    }
  }
}
```

#### Example [​](https://marketplace.gohighlevel.com/docs/webhook/TaskCreate/\#example "Direct link to Example")

```json
{
  "type": "TaskCreate",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "id": "UlRWGLSXh0ji5qbiGu4i",
  "assignedTo": "63e4qiWDsFJjOYAC8phG",
  "body": "Loram ipsum",
  "contactId": "CWBf1PR9LvvBkcYqiXlc",
  "title": "Loram ipsum",
  "dateAdded": "2021-11-26T12:41:02.193Z",
  "dueDate": "2021-11-26T12:41:02.193Z"
}
```

## Share your feedback

★★★★★