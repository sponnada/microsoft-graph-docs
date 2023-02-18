---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new AppRoleAssignedResourcesRequestBuilderGetRequestConfiguration();

$queryParameters = new AppRoleAssignedResourcesRequestBuilderGetQueryParameters();
$queryParameters->count = true;
$queryParameters->select = ["displayName","accountEnabled","servicePrincipalType","signInAudience"];

$headers = [
'ConsistencyLevel' => 'eventual',
];

$requestConfiguration->queryParameters = $queryParameters;
$requestConfiguration->headers = $headers;


$requestResult = $graphServiceClient->me()->appRoleAssignedResources()->get($requestConfiguration);


```