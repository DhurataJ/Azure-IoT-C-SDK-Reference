---                             
title: "IoTHubDeviceClient_LL_SetRetryPolicy function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_LL_SetRetryPolicy() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_LL_SetRetryPolicy()

Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client_ll.h](../iothub-device-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubDeviceClient_LL_SetRetryPolicy(
  IOTHUB_DEVICE_CLIENT_LL_HANDLE  iotHubClientHandle,
  IOTHUB_CLIENT_RETRY_POLICY      retryPolicy,
  size_t                          retryTimeoutLimitInSeconds
);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `retryPolicy` The policy to use to reconnect to IoT Hub when a connection drops. 

* `retryTimeoutLimitInSeconds` Maximum amount of time(seconds) to attempt reconnection when a connection drops to IOT Hub.

: Do not call [IoTHubDeviceClient_LL_Destroy()](../iothub-device-client-ll-h/iothubdeviceclient-ll-destroy.md) or [IoTHubDeviceClient_LL_DoWork()](../iothub-device-client-ll-h/iothubdeviceclient-ll-dowork.md) from inside your application's callback.

## Remarks
Uploads initiated by [IoTHubDeviceClient_LL_UploadToBlob()](../iothub-device-client-ll-h/iothubdeviceclient-ll-uploadtoblob.md) or [IoTHubDeviceClient_LL_UploadMultipleBlocksToBlob()](../iothub-device-client-ll-h/iothubdeviceclient-ll-uploadmultipleblockstoblob.md) do not have automatic retries and do not honor the retryPolicy settings.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

