---                             
title: "IoTHubDeviceClient_LL_GetLastMessageReceiveTime function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_LL_GetLastMessageReceiveTime() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/11/2018                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_LL_GetLastMessageReceiveTime()

This function returns in the out parameter lastMessageReceiveTime what was the value of the time function when the last message was received at the client.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client_ll.h](../iothub-device-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubDeviceClient_LL_GetLastMessageReceiveTime(
  IOTHUB_DEVICE_CLIENT_LL_HANDLE  iotHubClientHandle,
  time_t *                        lastMessageReceiveTime
);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `lastMessageReceiveTime` Out parameter containing the value of time function when the last message was received.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.
