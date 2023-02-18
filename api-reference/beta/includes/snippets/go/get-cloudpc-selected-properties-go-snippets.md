---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.DeviceManagementVirtualEndpointCloudPCItemRequestBuilderGetQueryParameters{
	Select: [] string {"id","displayName","imageDisplayName","lastModifiedDateTime","lastRemoteActionResult","lastLoginResult","connectivityResult"},
}
configuration := &graphconfig.DeviceManagementVirtualEndpointCloudPCItemRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.DeviceManagement().VirtualEndpoint().CloudPCsById("cloudPC-id").Get(context.Background(), configuration)


```