---                             
title: "IoTHubClient_GetRetryPolicy function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubClient_GetRetryPolicy() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubClient_GetRetryPolicy()

Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_client.h](../iothub-client-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubClient_GetRetryPolicy(IOTHUB_CLIENT_HANDLE  MU_IFCOMMA2);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `retryPolicy` Out parameter containing the policy to use to reconnect to IoT Hub. 

* `retryTimeoutLimitInSeconds` Out parameter containing maximum amount of time in seconds to attempt reconnection to IOT Hub.

**NOTE:** The application behavior is undefined if the user calls the [IoTHubClient_LL_Destroy](../iothub-client-ll-h/iothubclient-ll-destroy.md) function from within any callback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

