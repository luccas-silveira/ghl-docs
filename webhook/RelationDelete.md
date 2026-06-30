---
title: "Relationdelete"
source_url: https://marketplace.gohighlevel.com/docs/webhook/RelationDelete
version: v3
---
## Overview

This webhook response is triggered when an existing relation between objects is deleted.

For example, in a business management system, a company may want to remove an relation between a custom object record and a contact. In this case:

- The **first object** (custom object record) could represent an entity such as a project or a transaction.
- The **second object** (contact) would represent a person associated with the custom object.

## Schema

The webhook response follows the JSON schema below:

```json
{
  "type": "object",
  "properties": {
    "id": {
      "type": "string"
    },
    "firstObjectKey": {
      "type": "string"
    },
    "firstRecordId": {
      "type": "string"
    },
    "secondObjectKey": {
      "type": "string"
    },
    "secondRecordId": {
      "type": "string"
    },
    "associationId": {
      "type": "string"
    },
    "locationId": {
      "type": "string"
    },

  }
}
```

## Field Descriptions

### `id`

- Type: `string`
- Unique identifier for the deleted association.

### `firstObjectKey`

- Type: `string`
- Key representing the first object in the association.

### `firstRecordId`

- Type: `string`
- Identifier of the first object’s specific record.

### `secondObjectKey`

- Type: `string`
- Key representing the second object in the association.

### `secondRecordId`

- Type: `string`
- Identifier of the second object’s specific record.

### `associationId`

- Type: `string`
- Unique identifier for the association that was deleted.

### `locationId`

- Type: `string`
- Identifies the location associated with the deleted association.

## Example Response

```json
{
  "id": "67ae0d741119d218c9d0c477",
  "firstObjectKey": "custom_objects.mad",
  "firstRecordId": "67a349a79b28947ec1f65bb5",
  "secondObjectKey": "contact",
  "secondRecordId": "emqfhnG3g9D9chy9inTz",
  "associationId": "669e5795add2094075906c65",
  "locationId": "eHy2cOSZxMQzQ6Yyvl8P"
}
```

## Additional Notes

- The `firstObjectKey` and `secondObjectKey` define the relationship between the deleted entities.

## Share your feedback

★★★★★

- [Overview](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#overview)
- [Schema](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#schema)
- [Field Descriptions](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#field-descriptions)
  - [`id`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#id)
  - [`firstObjectKey`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#firstobjectkey)
  - [`firstRecordId`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#firstrecordid)
  - [`secondObjectKey`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#secondobjectkey)
  - [`secondRecordId`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#secondrecordid)
  - [`associationId`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#associationid)
  - [`locationId`](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#locationid)
- [Example Response](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#example-response)
- [Additional Notes](https://marketplace.gohighlevel.com/docs/webhook/RelationDelete/#additional-notes)