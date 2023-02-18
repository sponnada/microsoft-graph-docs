---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := abstractions.NewRequestHeaders()
headers.Add("Authorization", "Bearer {token}")

configuration := &graphconfig.TeamItemScheduleSwapShiftsChangeRequestsRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewSwapShiftsChangeRequest()
senderShiftId := "5ad10161-6524-4c7c-9beb-4e8677ba2f6d"
requestBody.SetSenderShiftId(&senderShiftId) 
senderMessage := "I can't make my shift, any chance we can swap?"
requestBody.SetSenderMessage(&senderMessage) 
recipientUserId := "567c8ea5-9e32-422a-a663-8270201699cd"
requestBody.SetRecipientUserId(&recipientUserId) 
recipientShiftId := "e73408ca-3ea5-4bbf-96a8-2e06c95f7a2c"
requestBody.SetRecipientShiftId(&recipientShiftId) 

result, err := graphClient.TeamsById("team-id").Schedule().SwapShiftsChangeRequests().Post(context.Background(), requestBody, configuration)


```