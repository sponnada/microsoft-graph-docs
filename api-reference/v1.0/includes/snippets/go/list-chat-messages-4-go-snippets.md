---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestTop := int32(2)
requestFilter := "lastModifiedDateTime ge 2022-09-22T00:00:00.000Z and lastModifiedDateTime le 2022-09-24T00:00:00.000Z"

requestParameters := &graphconfig.ChatItemMessagesRequestBuilderGetQueryParameters{
	Top: &requestTop,
	Orderby: [] string {"lastModifiedDateTime desc"},
	Filter: &requestFilter,
}
configuration := &graphconfig.ChatItemMessagesRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.ChatsById("chat-id").Messages().Get(context.Background(), configuration)


```