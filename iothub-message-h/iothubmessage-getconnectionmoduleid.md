---                             
title: "IoTHubMessage_GetConnectionModuleId function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_GetConnectionModuleId() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_GetConnectionModuleId()

Gets the module name from the IOTHUB_MESSAGE_HANDLE. No new memory is allocated, the caller is not responsible for freeing the memory. The memory is valid until IoTHubMessage_Destroy is called on the message.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
const char* IoTHubMessage_GetConnectionModuleId(IOTHUB_MESSAGE_HANDLE  MU_C2);
```

## Parameters
* `iotHubMessageHandle` Handle to the message.

## Return Value
A const char* pointing to the connection module Id.

