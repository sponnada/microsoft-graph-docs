---
title: "retentionEventStatus resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# retentionEventStatus resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|location|String|**TODO: Add Description**|
|status|retentionEventStatusType|**TODO: Add Description**. The possible values are: `none`, `inProcessing`, `failed`, `success`.|
|statusInformation|String|**TODO: Add Description**|
|workload|String|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.recordsManagement.retentionEventStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionEventStatus",
  "workload": "String",
  "location": "String",
  "status": "String",
  "statusInformation": "String"
}
```

