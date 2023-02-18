---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestFilter := "startswith(displayName,%20'A')"
requestTop := int32(2)

requestParameters := &graphconfig.TeamsRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
	Top: &requestTop,
}
configuration := &graphconfig.TeamsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Teams().Get(context.Background(), configuration)


```