---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewUser()
additionalData := map[string]interface{}{
ext55gb1l09_msLearnCourses := graphmodels.New()
courseType := "Admin"
ext55gb1l09_msLearnCourses.SetCourseType(&courseType) 
	requestBody.SetExt55gb1l09_msLearnCourses(ext55gb1l09_msLearnCourses)
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.UsersById("user-id").Patch(context.Background(), requestBody, nil)


```