---                             
title: "IoTHubModuleClient_SetConnectionStatusCallback function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubModuleClient_SetConnectionStatusCallback() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubModuleClient_SetConnectionStatusCallback()

Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_module_client.h](../iothub-module-client-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubModuleClient_SetConnectionStatusCallback(
  IOTHUB_MODULE_CLIENT_HANDLE               iotHubModuleClientHandle,
  IOTHUB_CLIENT_CONNECTION_STATUS_CALLBACK  connectionStatusCallback,
  void *                                    userContextCallback
);
```

## Parameters
* `iotHubModuleClientHandle` The handle created by a call to the create function. 

* `connectionStatusCallback` The callback specified by the module for receiving updates about the status of the connection to IoT Hub. 

* `userContextCallback` User specified context that will be provided to the callback. This can be NULL.

: Do not call [IoTHubModuleClient_Destroy()](../iothub-module-client-h/iothubmoduleclient-destroy.md) from inside your application's callback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

