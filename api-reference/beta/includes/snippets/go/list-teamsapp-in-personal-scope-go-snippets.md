---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestFilter := "appDefinitions/any"

requestParameters := &graphconfig.AppCatalogsTeamsAppsRequestBuilderGetQueryParameters{
	Expand: [] string {"appDefinitions($select=id,displayName,allowedInstallationScopes)"},
	Filter: &requestFilter,
}
configuration := &graphconfig.AppCatalogsTeamsAppsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.AppCatalogs().TeamsApps().Get(context.Background(), configuration)


```