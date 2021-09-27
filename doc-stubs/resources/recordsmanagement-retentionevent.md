---
title: "retentionEvent resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# retentionEvent resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/recordsmanagement-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List retentionEvents](../api/recordsmanagement-retentionevent-list.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md) collection|Get a list of the [retentionEvent](../resources/recordsmanagement-retentionevent.md) objects and their properties.|
|[Create retentionEvent](../api/recordsmanagement-retentionevent-create.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md)|Create a new [retentionEvent](../resources/recordsmanagement-retentionevent.md) object.|
|[Get retentionEvent](../api/recordsmanagement-retentionevent-get.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md)|Read the properties and relationships of a [retentionEvent](../resources/recordsmanagement-retentionevent.md) object.|
|[Update retentionEvent](../api/recordsmanagement-retentionevent-update.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md)|Update the properties of a [retentionEvent](../resources/recordsmanagement-retentionevent.md) object.|
|[Delete retentionEvent](../api/recordsmanagement-retentionevent-delete.md)|None|Deletes a [retentionEvent](../resources/recordsmanagement-retentionevent.md) object.|
|[List labels](../api/recordsmanagement-retentionevent-list-labels.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md) collection|Get the retentionLabel resources from the labels navigation property.|
|[Add retentionLabel](../api/recordsmanagement-retentionevent-post-labels.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md)|Add labels by posting to the labels collection.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|eventPropagationResult|[microsoft.graph.recordsManagement.eventPropagationResult](../resources/recordsmanagement-eventpropagationresult.md)|**TODO: Add Description**|
|eventStatus|[microsoft.graph.recordsManagement.retentionEventStatus](../resources/recordsmanagement-retentioneventstatus.md) collection|**TODO: Add Description**|
|eventTriggerDateTime|DateTimeOffset|**TODO: Add Description**|
|filesQuery|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md).|
|lastModifiedBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|lastStatusUpdateTime|DateTimeOffset|**TODO: Add Description**|
|messagesQuery|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|labels|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.recordsManagement.retentionEvent",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionEvent",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "messagesQuery": "String",
  "filesQuery": "String",
  "eventTriggerDateTime": "String (timestamp)",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "lastModifiedDateTime": "String (timestamp)",
  "eventPropagationResult": {
    "@odata.type": "microsoft.graph.recordsManagement.eventPropagationResult"
  },
  "eventStatus": [
    {
      "@odata.type": "microsoft.graph.recordsManagement.retentionEventStatus"
    }
  ],
  "lastStatusUpdateTime": "String (timestamp)"
}
```

