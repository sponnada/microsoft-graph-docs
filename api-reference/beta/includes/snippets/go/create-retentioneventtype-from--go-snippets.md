---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewRetentionEventType()
displayName := "String"
requestBody.SetDisplayName(&displayName) 
description := "String"
requestBody.SetDescription(&description) 
createdBy := graphmodels.NewIdentitySet()
requestBody.SetCreatedBy(createdBy)

result, err := graphClient.Security().TriggerTypes().RetentionEventTypes().Post(context.Background(), requestBody, nil)


```