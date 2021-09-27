---
title: "Create retentionEvent"
description: "Create a new retentionEvent object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create retentionEvent
Namespace: microsoft.graph.recordsManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new retentionEvent object.

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
POST /compliance/recordsManagement/events
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [retentionEvent](../resources/recordsmanagement-retentionevent.md) object.

The following table shows the properties that are required when you create the [retentionEvent](../resources/recordsmanagement-retentionevent.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/recordsmanagement-entity.md)|
|displayName|String|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|messagesQuery|String|**TODO: Add Description**|
|filesQuery|String|**TODO: Add Description**|
|eventTriggerDateTime|DateTimeOffset|**TODO: Add Description**|
|createdBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|lastModifiedBy|[microsoft.graph.identitySet](../resources/recordsmanagement-identityset.md)|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|eventPropagationResult|[microsoft.graph.recordsManagement.eventPropagationResult](../resources/recordsmanagement-eventpropagationresult.md)|**TODO: Add Description**|
|eventStatus|[microsoft.graph.recordsManagement.retentionEventStatus](../resources/recordsmanagement-retentioneventstatus.md) collection|**TODO: Add Description**|
|lastStatusUpdateTime|DateTimeOffset|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [retentionEvent](../resources/recordsmanagement-retentionevent.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_retentionevent_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/compliance/recordsManagement/events
Content-Type: application/json
Content-length: 594

{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionEvent",
  "displayName": "String",
  "description": "String",
  "messagesQuery": "String",
  "filesQuery": "String",
  "eventTriggerDateTime": "String (timestamp)",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
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


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.recordsManagement.retentionEvent"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.recordsManagement.retentionEvent",
  "id": "211aea61-ea61-211a-61ea-1a2161ea1a21",
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

