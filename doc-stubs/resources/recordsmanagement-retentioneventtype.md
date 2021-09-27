---
title: "retentionEventType resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# retentionEventType resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/recordsmanagement-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List retentionEventTypes](../api/recordsmanagement-retentioneventtype-list.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md) collection|Get a list of the [retentionEventType](../resources/recordsmanagement-retentioneventtype.md) objects and their properties.|
|[Create retentionEventType](../api/recordsmanagement-retentioneventtype-create.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|Create a new [retentionEventType](../resources/recordsmanagement-retentioneventtype.md) object.|
|[Get retentionEventType](../api/recordsmanagement-retentioneventtype-get.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|Read the properties and relationships of a [retentionEventType](../resources/recordsmanagement-retentioneventtype.md) object.|
|[Update retentionEventType](../api/recordsmanagement-retentioneventtype-update.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|Update the properties of a [retentionEventType](../resources/recordsmanagement-retentioneventtype.md) object.|
|[Delete retentionEventType](../api/recordsmanagement-retentioneventtype-delete.md)|None|Deletes a [retentionEventType](../resources/recordsmanagement-retentioneventtype.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md).|
|lastModifiedBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.recordsManagement.retentionEventType",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionEventType",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "lastModifiedDateTime": "String (timestamp)"
}
```

