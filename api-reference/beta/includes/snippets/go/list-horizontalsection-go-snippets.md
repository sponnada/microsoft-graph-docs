---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


result, err := graphClient.SitesById("site-id").PagesById("sitePage-id").CanvasLayout().HorizontalSections().Get(context.Background(), nil)


```