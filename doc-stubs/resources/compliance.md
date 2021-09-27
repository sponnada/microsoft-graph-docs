---
title: "compliance resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# compliance resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[Get compliance](../api/compliance-get.md)|[compliance](../resources/compliance.md)|Read the properties and relationships of a [compliance](../resources/compliance.md) object.|
|[Update compliance](../api/compliance-update.md)|[compliance](../resources/compliance.md)|Update the properties of a [compliance](../resources/compliance.md) object.|
|[List recordsManagementroot](../api/compliance-list-recordsmanagement.md)|[recordsManagementroot](../resources/recordsmanagementroot.md) collection|Get the recordsManagementroot resources from the recordsManagement navigation property.|
|[Create recordsManagementroot](../api/compliance-post-recordsmanagement.md)|[recordsManagementroot](../resources/recordsmanagementroot.md)|Create a new recordsManagementroot object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|ediscovery|[ediscoveryroot](../resources/ediscoveryroot.md)|**TODO: Add Description**|
|recordsManagement|[recordsManagementroot](../resources/recordsmanagementroot.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.compliance",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.compliance"
}
```

