---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAuthorizationPolicy()
allowEmailVerifiedUsersToJoinOrganization := false
requestBody.SetAllowEmailVerifiedUsersToJoinOrganization(&allowEmailVerifiedUsersToJoinOrganization) 

result, err := graphClient.Policies().AuthorizationPolicy().Patch(context.Background(), requestBody, nil)


```