---
title: "retentionLabel resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# retentionLabel resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/recordsmanagement-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List retentionLabels](../api/recordsmanagement-retentionlabel-list.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md) collection|Get a list of the [retentionLabel](../resources/recordsmanagement-retentionlabel.md) objects and their properties.|
|[Create retentionLabel](../api/recordsmanagement-retentionlabel-create.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md)|Create a new [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.|
|[Get retentionLabel](../api/recordsmanagement-retentionlabel-get.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md)|Read the properties and relationships of a [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.|
|[Update retentionLabel](../api/recordsmanagement-retentionlabel-update.md)|[microsoft.graph.recordsManagement.retentionLabel](../resources/recordsmanagement-retentionlabel.md)|Update the properties of a [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.|
|[Delete retentionLabel](../api/recordsmanagement-retentionlabel-delete.md)|None|Deletes a [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.|
|[List retentionEventType](../api/recordsmanagement-retentionlabel-list-eventtype.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md) collection|Get the retentionEventType resources from the eventType navigation property.|
|[Add retentionEventType](../api/recordsmanagement-retentionlabel-post-eventtype.md)|[microsoft.graph.recordsManagement.retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|Add eventType by posting to the eventType collection.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|actionAfterRetentionPeriod|actionAfterRetentionPeriod|**TODO: Add Description**. The possible values are: `none`, `delete`, `startDispositionReview`, `unknownFutureValue`.|
|behaviorDuringRetentionPeriod|behaviorDuringRetentionPeriod|**TODO: Add Description**. The possible values are: `doNotRetain`, `retain`, `retainAsRecord`, `retainAsRegulatoryRecord`, `unknownFutureValue`.|
|createdBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|descriptionForAdmins|String|**TODO: Add Description**|
|descriptionForUsers|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|dispositionReviewStages|[microsoft.graph.recordsManagement.dispositionReviewStage](../resources/recordsmanagement-dispositionreviewstage.md) collection|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md).|
|isInUse|Boolean|**TODO: Add Description**|
|lastModifiedBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|retentionDurationInDays|Int32|**TODO: Add Description**|
|retentionTrigger|retentionTrigger|**TODO: Add Description**. The possible values are: `dateLabeled`, `dateCreated`, `dateModified`, `dateOfEvent`, `unknownFutureValue`.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|eventType|[retentionEventType](../resources/recordsmanagement-retentioneventtype.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.recordsManagement.retentionLabel",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionLabel",
  "id": "String (identifier)",
  "displayName": "String",
  "behaviorDuringRetentionPeriod": "String",
  "actionAfterRetentionPeriod": "String",
  "retentionTrigger": "String",
  "retentionDurationInDays": "Integer",
  "isInUse": "Boolean",
  "descriptionForAdmins": "String",
  "descriptionForUsers": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "lastModifiedDateTime": "String (timestamp)",
  "dispositionReviewStages": [
    {
      "@odata.type": "microsoft.graph.recordsManagement.dispositionReviewStage"
    }
  ]
}
```

