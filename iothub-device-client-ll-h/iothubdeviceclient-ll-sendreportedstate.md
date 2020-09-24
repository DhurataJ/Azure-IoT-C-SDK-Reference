---                             
title: "IoTHubDeviceClient_LL_SendReportedState function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_LL_SendReportedState() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_LL_SendReportedState()

This API sends a report of the device's properties and their current values.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client_ll.h](../iothub-device-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubDeviceClient_LL_SendReportedState(
  IOTHUB_DEVICE_CLIENT_LL_HANDLE         iotHubClientHandle,
  const unsigned char *                  reportedState,
  size_t                                 size,
  IOTHUB_CLIENT_REPORTED_STATE_CALLBACK  reportedStateCallback,
  void *                                 userContextCallback
);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `reportedState` The current device property values to be 'reported' to the IoTHub. 

* `reportedStateCallback` The callback specified by the device client to be called with the result of the transaction. 

* `userContextCallback` User specified context that will be provided to the callback. This can be NULL.

**NOTE:** The application behavior is undefined if the user calls the [IoTHubDeviceClient_LL_Destroy](../iothub-device-client-ll-h/iothubdeviceclient-ll-destroy.md) function from within any callback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

