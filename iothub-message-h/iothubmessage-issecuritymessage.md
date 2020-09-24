---                             
title: "IoTHubMessage_IsSecurityMessage function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_IsSecurityMessage() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_IsSecurityMessage()

returns if this message is a IoTHub security message or not

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
bool IoTHubMessage_IsSecurityMessage(IOTHUB_MESSAGE_HANDLE  MU_C2);
```

## Parameters
* `iotHubMessageHandle` Handle to the message.

## Return Value
Returns true if the Message is a security message false otherwise.

