---                             
title: "IoTHubModuleClient_LL_SetModuleTwinCallback function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubModuleClient_LL_SetModuleTwinCallback() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubModuleClient_LL_SetModuleTwinCallback()

This API specifies a call back to be used when the module receives a desired state update.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_module_client_ll.h](../iothub-module-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubModuleClient_LL_SetModuleTwinCallback(
  IOTHUB_MODULE_CLIENT_LL_HANDLE      iotHubModuleClientHandle,
  IOTHUB_CLIENT_DEVICE_TWIN_CALLBACK  moduleTwinCallback,
  void *                              userContextCallback
);
```

## Parameters
* `iotHubModuleClientHandle` The handle created by a call to the create function. 

* `moduleTwinCallback` The callback specified by the module client to be used for updating the desired state. The callback will be called in response to patch request send by the IoT Hub services. The payload will be passed to the callback, along with two version numbers:

* Desired:

* LastSeenReported: 

* `userContextCallback` User specified context that will be provided to the callback. This can be NULL.

: Do not call [IoTHubModuleClient_LL_Destroy()](../iothub-module-client-ll-h/iothubmoduleclient-ll-destroy.md) or [IoTHubModuleClient_LL_DoWork()](../iothub-module-client-ll-h/iothubmoduleclient-ll-dowork.md) from inside your application's callback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

