---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAuthenticationMethodConfiguration()
state := graphmodels.ENABLED_AUTHENTICATIONMETHODSTATE 
requestBody.SetState(&state) 

result, err := graphClient.Policies().AuthenticationMethodsPolicy().AuthenticationMethodConfigurationsById("authenticationMethodConfiguration-id").Patch(context.Background(), requestBody, nil)


```