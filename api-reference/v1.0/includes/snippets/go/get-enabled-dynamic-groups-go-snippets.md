---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := abstractions.NewRequestHeaders()
headers.Add("ConsistencyLevel", "eventual")


requestFilter := "mailEnabled eq false and securityEnabled eq true and NOT) and membershipRuleProcessingState eq 'On'"
requestCount := true

requestParameters := &graphconfig.GroupsRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
	Count: &requestCount,
	Select: [] string {"id","membershipRule","membershipRuleProcessingState"},
}
configuration := &graphconfig.GroupsRequestBuilderGetRequestConfiguration{
	Headers: headers,
	QueryParameters: requestParameters,
}

result, err := graphClient.Groups().Get(context.Background(), configuration)


```