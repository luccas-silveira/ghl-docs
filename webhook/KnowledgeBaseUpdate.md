---
title: "Knowledgebaseupdate"
source_url: https://marketplace.gohighlevel.com/docs/webhook/KnowledgeBaseUpdate
version: v3
summary: "Called whenever a knowledge base name/description is updated"
---
Called whenever a knowledge base name/description is updated

#### Schema

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

#### Example

```json
{
  "type": "KnowledgeBaseUpdate",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "id": "6578278e879ad2646715ba9c",
  "name": "Support Knowledge Base",
  "description": "Updated FAQs and docs for customer support",
  "deleted": false
}
```

## Share your feedback

★★★★★