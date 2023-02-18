---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewGroup()
description := "Feelgood Marketing Campaign with external partners and vendors."
requestBody.SetDescription(&description) 
displayName := "Feelgood Marketing Campaign"
requestBody.SetDisplayName(&displayName) 
groupTypes := []string {
	"Unified",

}
requestBody.SetGroupTypes(groupTypes)
mailEnabled := true
requestBody.SetMailEnabled(&mailEnabled) 
mailNickname := "FeelGoodCampaign"
requestBody.SetMailNickname(&mailNickname) 
securityEnabled := true
requestBody.SetSecurityEnabled(&securityEnabled) 
additionalData := map[string]interface{}{
	"owners@odata.bind" := []string {
		"https://graph.microsoft.com/v1.0/users/cdb555e3-b33e-4fd5-a427-17fadacbdfa7",

	}
	"members@odata.bind" := []string {
		"https://graph.microsoft.com/v1.0/users/baf1b0a0-1f9a-4a56-9884-6a30824f8d20",

	}
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Groups().Post(context.Background(), requestBody, nil)


```