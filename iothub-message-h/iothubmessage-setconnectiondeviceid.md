---                             
title: "IoTHubMessage_SetConnectionDeviceId function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_SetConnectionDeviceId() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_SetConnectionDeviceId()

Sets connection device Id. CAUTION: SDK user should not call it directly, it is for internal use only.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
IOTHUB_MESSAGE_RESULT IoTHubMessage_SetConnectionDeviceId(IOTHUB_MESSAGE_HANDLE  MU_C2);
```

## Parameters
* `iotHubMessageHandle` Handle to the message. 

* `connectionDeviceId` Pointer to the device ID of connector

## Return Value
Returns IOTHUB_MESSAGE_OK if the DiagnosticData was set successfully or an error code otherwise.

