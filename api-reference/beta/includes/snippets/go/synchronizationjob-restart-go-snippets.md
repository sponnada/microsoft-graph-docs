---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := abstractions.NewRequestHeaders()
headers.Add("Authorization", "Bearer <token>")

configuration := &graphconfig.ServicePrincipalItemSynchronizationJobItemMicrosoft.graph.restartRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewRestartPostRequestBody()
criteria := graphmodels.NewSynchronizationJobRestartCriteria()
resetScope := graphmodels.WATERMARK, ESCROWS, QUARANTINESTATE_SYNCHRONIZATIONJOBRESTARTSCOPE 
criteria.SetResetScope(&resetScope) 
requestBody.SetCriteria(criteria)

graphClient.ServicePrincipalsById("servicePrincipal-id").Synchronization().JobsById("synchronizationJob-id").Restart().Post(context.Background(), requestBody, configuration)


```