---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestTop := int32(100)
requestSkip := int32(0)

requestParameters := &graphconfig.IdentityGovernanceAccessReviewsDefinitionItemInstancesRequestBuilderGetQueryParameters{
	Top: &requestTop,
	Skip: &requestSkip,
}
configuration := &graphconfig.IdentityGovernanceAccessReviewsDefinitionItemInstancesRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.IdentityGovernance().AccessReviews().DefinitionsById("accessReviewScheduleDefinition-id").Instances().Get(context.Background(), configuration)


```