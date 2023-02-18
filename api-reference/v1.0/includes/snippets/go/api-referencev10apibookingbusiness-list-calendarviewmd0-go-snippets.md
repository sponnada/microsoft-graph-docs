---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestStart := "2018-04-30T00:00:00Z"
requestEnd := "2018-05-10T00:00:00Z"

requestParameters := &graphconfig.SolutionsBookingBusinesseItemCalendarViewRequestBuilderGetQueryParameters{
	Start: &requestStart,
	End: &requestEnd,
}
configuration := &graphconfig.SolutionsBookingBusinesseItemCalendarViewRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Solutions().BookingBusinessesById("bookingBusiness-id").CalendarView().Get(context.Background(), configuration)


```