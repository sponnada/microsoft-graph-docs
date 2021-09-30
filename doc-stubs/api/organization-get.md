---
title: "Get organization"
description: "Read the properties and relationships of an organization object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get organization
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of an [organization](../resources/organization.md) object.

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
GET /organization/{organizationId}
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and an [organization](../resources/organization.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_organization"
}
-->
``` http
GET https://graph.microsoft.com/beta/organization/{organizationId}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Microsoft.DirectoryServices.organization"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#Microsoft.DirectoryServices.organization",
    "id": "c489cbe1-cbe1-c489-e1cb-89c4e1cb89c4",
    "deletedDateTime": "String (timestamp)",
    "assignedPlans": [
      {
        "@odata.type": "microsoft.graph.assignedPlan"
      }
    ],
    "businessPhones": [
      "String"
    ],
    "city": "String",
    "companyTags": [
      "String"
    ],
    "country": "String",
    "countryLetterCode": "String",
    "createdDateTime": "String (timestamp)",
    "dataBoundary": "String",
    "directorySizeQuota": {
      "@odata.type": "microsoft.graph.directorySizeQuota"
    },
    "displayName": "String",
    "isMultipleDataLocationsForServicesEnabled": "Boolean",
    "licenseMigrationInfo": {
      "@odata.type": "microsoft.graph.licenseMigrationInfo"
    },
    "marketingNotificationEmails": [
      "String"
    ],
    "onPremisesLastSyncDateTime": "String (timestamp)",
    "onPremisesSyncEnabled": "Boolean",
    "postalCode": "String",
    "preferredLanguage": "String",
    "privacyProfile": {
      "@odata.type": "microsoft.graph.privacyProfile"
    },
    "provisionedPlans": [
      {
        "@odata.type": "microsoft.graph.provisionedPlan"
      }
    ],
    "releaseTrack": "String",
    "replicationScope": "String",
    "securityComplianceNotificationMails": [
      "String"
    ],
    "securityComplianceNotificationPhones": [
      "String"
    ],
    "state": "String",
    "street": "String",
    "technicalNotificationMails": [
      "String"
    ],
    "verifiedDomains": [
      {
        "@odata.type": "microsoft.graph.verifiedDomain"
      }
    ]
  }
}
```

