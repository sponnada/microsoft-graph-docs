---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewPlannerPlanConfiguration()
defaultLanguage := "en-us"
requestBody.SetDefaultLanguage(&defaultLanguage) 


plannerPlanConfigurationBucketDefinition := graphmodels.NewPlannerPlanConfigurationBucketDefinition()
externalBucketId := "deliveryBucket"
plannerPlanConfigurationBucketDefinition.SetExternalBucketId(&externalBucketId) 
plannerPlanConfigurationBucketDefinition1 := graphmodels.NewPlannerPlanConfigurationBucketDefinition()
externalBucketId := "storePickupBucket"
plannerPlanConfigurationBucketDefinition1.SetExternalBucketId(&externalBucketId) 
plannerPlanConfigurationBucketDefinition2 := graphmodels.NewPlannerPlanConfigurationBucketDefinition()
externalBucketId := "specialOrdersBucket"
plannerPlanConfigurationBucketDefinition2.SetExternalBucketId(&externalBucketId) 
plannerPlanConfigurationBucketDefinition3 := graphmodels.NewPlannerPlanConfigurationBucketDefinition()
externalBucketId := "returnProcessingBucket"
plannerPlanConfigurationBucketDefinition3.SetExternalBucketId(&externalBucketId) 

buckets := []graphmodels.PlannerPlanConfigurationBucketDefinitionable {
	plannerPlanConfigurationBucketDefinition,
	plannerPlanConfigurationBucketDefinition1,
	plannerPlanConfigurationBucketDefinition2,
	plannerPlanConfigurationBucketDefinition3,

}
requestBody.SetBuckets(buckets)

result, err := graphClient.Solutions().BusinessScenariosById("businessScenario-id").Planner().PlanConfiguration().Patch(context.Background(), requestBody, nil)


```