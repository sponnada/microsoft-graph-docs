---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestFilter := "languageTag eq 'en-us'"

requestParameters := &graphconfig.SolutionsBusinessScenarioItemPlannerPlanConfigurationLocalizationsRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
}
configuration := &graphconfig.SolutionsBusinessScenarioItemPlannerPlanConfigurationLocalizationsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Solutions().BusinessScenariosById("businessScenario-id").Planner().PlanConfiguration().Localizations().Get(context.Background(), configuration)


```