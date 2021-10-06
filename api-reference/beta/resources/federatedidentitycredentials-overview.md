---
title: "Federated identity credentials in Azure Active Directory (Azure AD)"
description: "Represents a federated identity credential on an application."
author: "kjyam98"
localization_priority: Normal
ms.prod: "applications"
doc_type: conceptualPageType
---

# Federated identity credentials in Azure Active Directory (preview)

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Today, developers can use certificates or client secrets for their application's credentials. Federated identity credentials are a new type of credential that will allow the impersonation of an Azure Active Directory (Azure AD) application. This credential will be used to exchange a token from a trusted issuer for an access token of an Azure AD application.

Key scenarios for federated identity credentials:
1) Cross-tenant Customer Managed Keys for Independent Software Vendors (ISVs): with federated identities on multi-tenant Azure AD applications, a managed identity can impersonate an application in the tenants in which the application is installed, and get tokens on behalf of the application.
   
2) Exchanging Kubernetes service account tokens for Azure AD access tokens: set a federated identity on an Azure AD application allowing a Kubernetes trusted token to assume that application and get token to access resources.
   
3) Exchanging GitHub tokens for Azure AD access tokens: set a federated identity on an Azure AD application allowing a GitHub Actions workflow to deploy resources associated with that application.

Federated identity credentials are supported on applications only.




## See also

+ [Workload identity federation](/azure/active-directory/develop/workload-identity-federation)