---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAttachment()
name := "menu.txt"
requestBody.SetName(&name) 
additionalData := map[string]interface{}{
	"contentBytes" : "bWFjIGFuZCBjaGVlc2UgdG9kYXk=", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().Outlook().TasksById("outlookTask-id").Attachments().Post(context.Background(), requestBody, nil)


```