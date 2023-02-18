---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.UserItemRequestBuilderGetQueryParameters{
	Select: [] string {"id","displayName","extkmpdyld2_graphLearnCourses"},
}
configuration := &graphconfig.UserItemRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.UsersById("user-id").Get(context.Background(), configuration)


```