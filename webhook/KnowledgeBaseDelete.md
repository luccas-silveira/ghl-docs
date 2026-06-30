---
title: "Knowledgebasedelete"
source_url: https://marketplace.gohighlevel.com/docs/webhook/KnowledgeBaseDelete
version: v3
---
Called whenever a knowledge base is deleted

#### Schema [​](https://marketplace.gohighlevel.com/docs/webhook/KnowledgeBaseDelete/\#schema "Direct link to Schema")

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
    "name": {
      "type": "string"
    },
    "description": {
      "type": "string"
    },
    "deleted": {
      "type": "boolean"
    }
  }
}
```

#### Example [​](https://marketplace.gohighlevel.com/docs/webhook/KnowledgeBaseDelete/\#example "Direct link to Example")

```json
{
  "type": "KnowledgeBaseDelete",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "id": "6578278e879ad2646715ba9c",
  "name": "Support Knowledge Base",
  "description": "FAQs and docs for customer support",
  "deleted": true
}
```

## Share your feedback

★★★★★