---
title: "Update retentionLabel"
description: "Update the properties of a retentionLabel object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update retentionLabel
Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /compliance/recordsManagement/labels/{retentionLabelId}
PATCH /compliance/recordsManagement/events/{retentionEventId}/labels/{retentionLabelId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object.

The following table shows the properties that are required when you update the [retentionLabel](../resources/recordsmanagement-retentionlabel.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md)|
|displayName|String|**TODO: Add Description**|
|behaviorDuringRetentionPeriod|behaviorDuringRetentionPeriod|**TODO: Add Description**. The possible values are: `doNotRetain`, `retain`, `retainAsRecord`, `retainAsRegulatoryRecord`, `unknownFutureValue`.|
|actionAfterRetentionPeriod|actionAfterRetentionPeriod|**TODO: Add Description**. The possible values are: `none`, `delete`, `startDispositionReview`, `unknownFutureValue`.|
|retentionTrigger|retentionTrigger|**TODO: Add Description**. The possible values are: `dateLabeled`, `dateCreated`, `dateModified`, `dateOfEvent`, `unknownFutureValue`.|
|retentionDurationInDays|Int32|**TODO: Add Description**|
|isInUse|Boolean|**TODO: Add Description**|
|descriptionForAdmins|String|**TODO: Add Description**|
|descriptionForUsers|String|**TODO: Add Description**|
|createdBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|lastModifiedBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|dispositionReviewStages|[microsoft.graph.recordsManagement.dispositionReviewStage](../resources/recordsmanagement-dispositionreviewstage.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [retentionLabel](../resources/recordsmanagement-retentionlabel.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_retentionlabel"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/compliance/recordsManagement/labels/{retentionLabelId}
Content-Type: application/json
Content-length: 570

{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionLabel",
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
  "dispositionReviewStages": [
    {
      "@odata.type": "microsoft.graph.recordsManagement.dispositionReviewStage"
    }
  ]
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionLabel",
  "id": "6fb1c04e-c04e-6fb1-4ec0-b16f4ec0b16f",
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

