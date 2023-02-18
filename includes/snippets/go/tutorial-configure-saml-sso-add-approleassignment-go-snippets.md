---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAppRoleAssignment()
principalId := uuid.MustParse("040f9599-7c0f-4f94-aa75-8394c4c6ea9b")
requestBody.SetPrincipalId(&principalId) 
principalType := "User"
requestBody.SetPrincipalType(&principalType) 
appRoleId := uuid.MustParse("3a84e31e-bffa-470f-b9e6-754a61e4dc63")
requestBody.SetAppRoleId(&appRoleId) 
resourceId := uuid.MustParse("a750f6cf-2319-464a-bcc3-456926736a91")
requestBody.SetResourceId(&resourceId) 

result, err := graphClient.ServicePrincipalsById("servicePrincipal-id").AppRoleAssignments().Post(context.Background(), requestBody, nil)


```