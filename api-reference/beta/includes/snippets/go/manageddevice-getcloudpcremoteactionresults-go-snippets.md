---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


result, err := graphClient.DeviceManagement().ManagedDevicesById("managedDevice-id").GetCloudPcRemoteActionResults().Get(context.Background(), nil)


```