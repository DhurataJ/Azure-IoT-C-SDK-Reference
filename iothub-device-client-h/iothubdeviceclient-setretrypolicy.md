---                             
title: "IoTHubDeviceClient_SetRetryPolicy function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_SetRetryPolicy() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_SetRetryPolicy()

Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client.h](../iothub-device-client-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubDeviceClient_SetRetryPolicy(
  IOTHUB_DEVICE_CLIENT_HANDLE  iotHubClientHandle,
  IOTHUB_CLIENT_RETRY_POLICY   retryPolicy,
  size_t                       retryTimeoutLimitInSeconds
);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `retryPolicy` The policy to use to reconnect to IoT Hub when a connection drops. 

* `retryTimeoutLimitInSeconds` Maximum amount of time(seconds) to attempt reconnection when a connection drops to IOT Hub.

: Do not call [IoTHubDeviceClient_Destroy()](../iothub-device-client-h/iothubdeviceclient-destroy.md) from inside your application's callback.

## Remarks
Uploads initiated by IoTHubDeviceClient_UploadToBlob or IoTHubDeviceClient_UploadMultipleBlocksToBlob do not have automatic retries and do not honor the retryPolicy settings.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

