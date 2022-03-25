---                             
title: "IoTHubDeviceClient_SetMessageCallback function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_SetMessageCallback() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_SetMessageCallback()

Sets up the message callback to be invoked when IoT Hub issues a message to the device. This is a blocking call.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client.h](../iothub-device-client-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubDeviceClient_SetMessageCallback(
  IOTHUB_DEVICE_CLIENT_HANDLE           iotHubClientHandle,
  IOTHUB_CLIENT_MESSAGE_CALLBACK_ASYNC  messageCallback,
  void *                                userContextCallback
);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `messageCallback` The callback specified by the device for receiving messages from IoT Hub. 

* `userContextCallback` User specified context that will be provided to the callback. This can be NULL.

: Do not call [IoTHubDeviceClient_Destroy()](../iothub-device-client-h/iothubdeviceclient-destroy.md) from inside your application's callback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

