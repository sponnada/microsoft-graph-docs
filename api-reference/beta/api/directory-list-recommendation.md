---
title: "List recommendations"
description: "Get a list of the recommendation objects and their properties."
author: "hafowler"
ms.localizationpriority: medium
ms.prod: "identity-and-access"
doc_type: apiPageType
---

# List recommendations
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [recommendation](../resources/recommendation.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DirectoryRecommendations.Read.All, DirectoryRecommendations.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|DirectoryRecommendations.Read.All, DirectoryRecommendations.ReadWrite.All|

For delegated scenarios, the admin needs one of the following [Azure AD roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
- Global administrator
- Global reader
- Security administrator
- Security operator
- Security reader
- Application administrator
- Cloud application administrator
- Reports reader

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /directory/recommendations
```

## Optional query parameters
This method supports `$select` and `$filter` OData query parameters to help customize the response. `$expand` is supported by the **impactedResources** relationship. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [recommendation](../resources/recommendation.md) objects in the response body.

## Examples

### Example 1: Get the list of recommendations

#### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "list_recommendation"
}
-->
``` http
GET https://graph.microsoft.com/beta/directory/recommendations
```


#### Response
The following is an example of the response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.recommendation)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#directory/recommendations",
  "value": [
    {
      "id": "0cb31920-84b9-471f-a6fb-468c1a847088_Microsoft.Identity.IAM.Insights.TurnOffPerUserMFA",
      "recommendationType": "turnOffPerUserMFA",
      "createdDateTime": "2022-02-28T02:53:00Z",
      "impactStartDateTime": "2022-02-28T02:53:00Z",
      "postponeUntilDateTime": null,
      "lastModifiedDateTime": "2023-01-10T22:57:10.2509132Z",
      "lastModifiedBy": "b5fa65db-0d2b-4233-8788-ab0213567669",
      "currentScore": 0.0,
      "maxScore": 5.0,
      "displayName": "Convert from per-user MFA to Conditional Access MFA",
      "featureAreas": [
          "conditionalAccess"
      ],
      "insights": "13 users are currently configured for per-user Multi-Factor Authentication (MFA). However, there are 6 users configured for Conditional Access (CA) MFA. The per-user MFA configuration supersedes the MFA settings applied via CA policies, potentially creating unnecessary MFA prompts.",
      "benefits": "Improve user productivity and minimize sign-in time with fewer MFA prompts. Ensure that your most sensitive resources can have the tighest controls, while your least sensitive resources can be more freely accessible.",
      "category": "identityBestPractice",
      "status": "active",
      "priority": "medium",
      "impactType": "users",
      "remediationImpact": "",
      "actionSteps": [
        {
          "stepNumber": 1,
          "text": "1. To get started, confirm that there is an existing CA policy with an MFA requirement. Ensure that you are covering all resources and users you would like to secure with MFA.",
          "actionUrl": {
              "displayName": "Click here to view your CA policies",
              "url": "https://portal.azure.com/#blade/Microsoft_AAD_IAM/PoliciesTemplateBlade"
          }
        },
        {
          "stepNumber": 2,
          "text": "2. To require MFA via a CA policy, follow the steps in this tutorial.",
          "actionUrl": {
              "displayName": "Secure user sign-in events with Azure AD Multi-Factor Authentication",
              "url": "https://docs.microsoft.com/en-us/azure/active-directory/authentication/tutorial-enable-azure-mfa?toc=/azure/active-directory/conditional-access/toc.json&bc=/azure/active-directory/conditional-access/breadcrumb/toc.json"
          }
        },
        {
          "stepNumber": 3,
          "text": "3. Ensure that the per-user MFA configuration is turned off",
          "actionUrl": {
              "displayName": "Navigate to MFA settings.",
              "url": "https://account.activedirectory.windowsazure.com/UserManagement/MfaSettings.aspx"
          }
        }
      ]
    },
  ]        
}
```
### Example 2: Get a recommendation object without its associated resources by the recommendationType

#### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "get_recommendation"
}
-->
``` http
GET https://graph.microsoft.com/beta/directory/recommendations?$filter=recommendationType eq 'turnOffPerUserMFA'
```

#### Response
The following is an example of the response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.recommendation"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#directory/recommendations/$entity",
  "id": "0cb31920-84b9-471f-a6fb-468c1a847088_Microsoft.Identity.IAM.Insights.TurnOffPerUserMFA",
  "recommendationType": "turnOffPerUserMFA",
  "createdDateTime": "2022-02-28T02:53:00Z",
  "impactStartDateTime": "2022-02-28T02:53:00Z",
  "postponeUntilDateTime": null,
  "lastModifiedDateTime": "2023-01-10T22:57:10.2509132Z",
  "lastModifiedBy": "d5a3853c-8e04-42b6-a530-bf159e99174a",
  "currentScore": 0.0,
  "maxScore": 5.0,
  "displayName": "Convert from per-user MFA to Conditional Access MFA",
  "featureAreas": [
    "conditionalAccess"
  ],
  "insights": "13 users are currently configured for per-user Multi-Factor Authentication (MFA)...",
  "benefits": "Improve user productivity and minimize sign-in time with fewer MFA prompts...",
  "category": "identityBestPractice",
  "status": "active",
  "priority": "medium",
  "impactType": "users",
  "remediationImpact": "",
  "actionSteps": [
    {
      "stepNumber": 1,
      "text": "1. To get started, confirm that...",
      "actionUrl": {
        "displayName": "Click here to view your CA policies",
        "url": "https://portal.azure.com/#blade/Microsoft_AAD_IAM/PoliciesTemplateBlade"
      }
    },
    {
      "stepNumber": 2,
      "text": "2. To require MFA via a CA policy, follow the steps in this tutorial.",
      "actionUrl": {
          "displayName": "Secure user sign-in events with Azure AD Multi-Factor Authentication",
          "url": "https://docs.microsoft.com/en-us/azure/active-directory/authentication/tutorial-enable-azure-mfa?toc=/azure/active-directory/conditional-access/toc.json&bc=/azure/active-directory/conditional-access/breadcrumb/toc.json"
      }
    },
    {
      "stepNumber": 3,
      "text": "3. Ensure that the per-user MFA configuration is turned off",
      "actionUrl": {
          "displayName": "Navigate to MFA settings.",
          "url": "https://account.activedirectory.windowsazure.com/UserManagement/MfaSettings.aspx"
      }
    }
  ]
}
```

### Example 3: Get a recommendation object with its associated impacted resources

#### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "get_recommendation"
}
-->
``` http
GET https://graph.microsoft.com/beta/directory/recommendations?$filter=id eq '0cb31920-84b9-471f-a6fb-468c1a847088_Microsoft.Identity.IAM.Insights.TurnOffPerUserMFA'&$expand=impactedResources
```

#### Response
The following is an example of the response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.recommendation"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#directory/recommendations(impactedResources())",
  "id": "0cb31920-84b9-471f-a6fb-468c1a847088_Microsoft.Identity.IAM.Insights.TurnOffPerUserMFA",
  "recommendationType": "turnOffPerUserMFA",
  "createdDateTime": "2022-02-28T02:53:00Z",
  "impactStartDateTime": "2022-02-28T02:53:00Z",
  "postponeUntilDateTime": null,
  "lastModifiedDateTime": "2023-01-10T22:57:10.2509132Z",
  "lastModifiedBy": "d5a3853c-8e04-42b6-a530-bf159e99174a",
  "currentScore": 0.0,
  "maxScore": 5.0,
  "displayName": "Convert from per-user MFA to Conditional Access MFA",
  "featureAreas": [
    "conditionalAccess"
  ],
  "insights": "13 users are currently configured for per-user Multi-Factor Authentication (MFA). However, there are 6 users configured for Conditional Access (CA) MFA. The per-user MFA configuration supersedes the MFA settings applied via CA policies, potentially creating unnecessary MFA prompts.",
  "benefits": "Improve user productivity and minimize sign-in time with fewer MFA prompts. Ensure that your most sensitive resources can have the tighest controls, while your least sensitive resources can be more freely accessible.",
  "category": "identityBestPractice",
  "status": "active",
  "priority": "medium",
  "impactType": "users",
  "remediationImpact": "",
  "actionSteps": [
    {
      "stepNumber": 1,
      "text": "1. To get started, confirm that there is an existing CA policy with an MFA requirement. Ensure that you are covering all resources and users you would like to secure with MFA.",
      "actionUrl": {
        "displayName": "Click here to view your CA policies",
        "url": "https://portal.azure.com/#blade/Microsoft_AAD_IAM/PoliciesTemplateBlade"
      }
    },
    {
      "stepNumber": 2,
      "text": "2. To require MFA via a CA policy, follow the steps in this tutorial.",
      "actionUrl": {
          "displayName": "Secure user sign-in events with Azure AD Multi-Factor Authentication",
          "url": "https://docs.microsoft.com/en-us/azure/active-directory/authentication/tutorial-enable-azure-mfa?toc=/azure/active-directory/conditional-access/toc.json&bc=/azure/active-directory/conditional-access/breadcrumb/toc.json"
      }
    },
    {
      "stepNumber": 3,
      "text": "3. Ensure that the per-user MFA configuration is turned off",
      "actionUrl": {
          "displayName": "Navigate to MFA settings.",
          "url": "https://account.activedirectory.windowsazure.com/UserManagement/MfaSettings.aspx"
      }
    }
  ],
  "impactedResources@odata.context": "https://graph.microsoft.com/beta/$metadata#directory/recommendations('0cb31920-84b9-471f-a6fb-468c1a847088_Microsoft.Identity.IAM.Insights.TurnOffPerUserMFA')/impactedResources",
  "impactedResources": []
}
```
