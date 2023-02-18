---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewGroup()
description := "Marketing group"
requestBody.SetDescription(&description) 
displayName := "Marketing resources"
requestBody.SetDisplayName(&displayName) 
mailEnabled := false
requestBody.SetMailEnabled(&mailEnabled) 
mailNickname := "markres"
requestBody.SetMailNickname(&mailNickname) 
securityEnabled := true
requestBody.SetSecurityEnabled(&securityEnabled) 

result, err := graphClient.Groups().Post(context.Background(), requestBody, nil)


```