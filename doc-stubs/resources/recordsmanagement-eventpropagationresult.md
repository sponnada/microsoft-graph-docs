---
title: "eventPropagationResult resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# eventPropagationResult resource type

Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|error|[microsoft.graph.recordsManagement.publicError](../resources/recordsmanagement-synchronization-publicerror.md)|**TODO: Add Description**|
|status|eventPropagationStatus|**TODO: Add Description**. The possible values are: `pending`, `error`, `success`, `notAvaliable`.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.recordsManagement.eventPropagationResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.recordsManagement.eventPropagationResult",
  "error": {
    "@odata.type": "microsoft.graph.recordsManagement.publicError"
  },
  "status": "String"
}
```

