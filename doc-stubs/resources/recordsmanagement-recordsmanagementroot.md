---
title: "recordsManagementroot resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# recordsManagementroot resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/recordsmanagement-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List recordsManagementroots](../api/recordsmanagement-recordsmanagementroot-list.md)|[microsoft.graph.recordsManagement.recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) collection|Get a list of the [recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) objects and their properties.|
|[Create recordsManagementroot](../api/recordsmanagement-recordsmanagementroot-create.md)|[microsoft.graph.recordsManagement.recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md)|Create a new [recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) object.|
|[Get recordsManagementroot](../api/recordsmanagement-recordsmanagementroot-get.md)|[microsoft.graph.recordsManagement.recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md)|Read the properties and relationships of a [recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) object.|
|[Update recordsManagementroot](../api/recordsmanagement-recordsmanagementroot-update.md)|[microsoft.graph.recordsManagement.recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md)|Update the properties of a [recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) object.|
|[Delete recordsManagementroot](../api/recordsmanagement-recordsmanagementroot-delete.md)|None|Deletes a [recordsManagementroot](../resources/recordsmanagement-recordsmanagementroot.md) object.|
|[List events](../api/recordsmanagement-recordsmanagementroot-list-events.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md) collection|Get the retentionEvent resources from the events navigation property.|
|[Create retentionEvent](../api/recordsmanagement-recordsmanagementroot-post-events.md)|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md)|Create a new retentionEvent object.|
|[List eventTypes](../api/recordsmanagement-recordsmanagementroot-list-eventtypes.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md) collection|Get the retentionEventType resources from the eventTypes navigation property.|
|[Create retentionEventType](../api/recordsmanagement-recordsmanagementroot-post-eventtypes.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|Create a new retentionEventType object.|
|[List labels](../api/recordsmanagement-recordsmanagementroot-list-labels.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md) collection|Get the retentionLabel resources from the labels navigation property.|
|[Create retentionLabel](../api/recordsmanagement-recordsmanagementroot-post-labels.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md)|Create a new retentionLabel object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md).|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|events|[microsoft.graph.recordsManagement.retentionEvent](../resources/recordsmanagement-retentionevent.md) collection|**TODO: Add Description**|
|eventTypes|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md) collection|**TODO: Add Description**|
|labels|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.recordsManagement.recordsManagementroot",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.recordsManagementroot",
  "id": "String (identifier)"
}
```

