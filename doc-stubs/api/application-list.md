---
title: "List applications"
description: "Get a list of the application objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List applications
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [application](../resources/application.md) objects and their properties.

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
GET /applications
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

If successful, this method returns a `200 OK` response code and a collection of [application](../resources/application.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_application"
}
-->
``` http
GET https://graph.microsoft.com/beta/applications
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(Microsoft.DirectoryServices.application)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#Microsoft.DirectoryServices.application",
      "id": "22c9d472-d472-22c9-72d4-c92272d4c922",
      "deletedDateTime": "String (timestamp)",
      "api": {
        "@odata.type": "microsoft.graph.apiApplication"
      },
      "appId": "String",
      "appMetadata": {
        "@odata.type": "microsoft.graph.appMetadata"
      },
      "appRoles": [
        {
          "@odata.type": "microsoft.graph.appRole"
        }
      ],
      "createdDateTime": "String (timestamp)",
      "description": "String",
      "disabledByMicrosoftStatus": "String",
      "isFallbackPublicClient": "Boolean",
      "identifierUris": [
        "String"
      ],
      "defaultRedirectUri": "String",
      "displayName": "String",
      "expectsForwardableIdTokens": "Boolean",
      "groupMembershipClaims": "String",
      "info": {
        "@odata.type": "microsoft.graph.informationalUrl"
      },
      "isDeviceOnlyAuthSupported": "Boolean",
      "isManagementRestricted": "Boolean",
      "keyCredentials": [
        {
          "@odata.type": "microsoft.graph.keyCredential"
        }
      ],
      "legacyAllowPassthroughUsers": "Boolean",
      "logo": "Stream",
      "microsoftPolicyGroup": "Boolean",
      "notes": "String",
      "optionalClaims": {
        "@odata.type": "microsoft.graph.optionalClaims"
      },
      "parentalControlSettings": {
        "@odata.type": "microsoft.graph.parentalControlSettings"
      },
      "passwordCredentials": [
        {
          "@odata.type": "microsoft.graph.passwordCredential"
        }
      ],
      "publicClient": {
        "@odata.type": "microsoft.graph.publicClientApplication"
      },
      "publisherDomain": "String",
      "requiredResourceAccess": [
        {
          "@odata.type": "microsoft.graph.requiredResourceAccess"
        }
      ],
      "servicePrincipalLifecyclePolicy": "String",
      "serviceTreeId": "String",
      "signInAudience": "String",
      "spa": {
        "@odata.type": "microsoft.graph.spaApplication"
      },
      "tags": [
        "String"
      ],
      "tokenEncryptionKeyId": "Guid",
      "trustedSubjectNameAndIssuers": [
        {
          "@odata.type": "microsoft.graph.trustedSubjectNameAndIssuer"
        }
      ],
      "uniqueName": "String",
      "verifiedPublisher": {
        "@odata.type": "microsoft.graph.verifiedPublisher"
      },
      "web": {
        "@odata.type": "microsoft.graph.webApplication"
      }
    }
  ]
}
```

