---                             
title: "IoTHubMessage_GetString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_GetString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_GetString()

Returns the null terminated string stored in the message. If the content type of the message is not IOTHUBMESSAGE_STRING then the function returns NULL. No new memory is allocated, the caller is not responsible for freeing the memory. The memory is valid until IoTHubMessage_Destroy is called on the message.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
const char* IoTHubMessage_GetString(IOTHUB_MESSAGE_HANDLE  iotHubMessageHandle);
```

## Parameters
* `iotHubMessageHandle` Handle to the message.

## Return Value
NULL if an error occurs or a pointer to the stored null terminated string otherwise.

