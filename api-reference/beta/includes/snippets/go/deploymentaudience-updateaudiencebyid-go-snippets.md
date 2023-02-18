---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewUpdateAudienceByIdPostRequestBody()
memberEntityType := "String"
requestBody.SetMemberEntityType(&memberEntityType) 
addMembers := []string {
	"String",

}
requestBody.SetAddMembers(addMembers)
removeMembers := []string {
	"String",

}
requestBody.SetRemoveMembers(removeMembers)
addExclusions := []string {
	"String",

}
requestBody.SetAddExclusions(addExclusions)
removeExclusions := []string {
	"String",

}
requestBody.SetRemoveExclusions(removeExclusions)

graphClient.Admin().Windows().Updates().DeploymentsById("deployment-id").Audience().UpdateAudienceById().Post(context.Background(), requestBody, nil)


```