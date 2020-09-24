---                             
title: "IoTHubMessage_SetProperty function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_SetProperty() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_SetProperty()

Sets a property on a Iothub Message.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
IOTHUB_MESSAGE_RESULT IoTHubMessage_SetProperty(IOTHUB_MESSAGE_HANDLE  MU_IFCOMMA2);
```

## Parameters
* `iotHubMessageHandle` Handle to the message.

* `key` name of the property to set. Note that when sending messages via the HTTP transport, this value must not contain spaces.

* `value` of the property to set.

**NOTE:** Property names and values must not contain spaces and can only contain ASCII alphanumeric characters, plus {'!', '#', '$', '%, '&', ''', '*', '+', '-', '.', '^', '_', '`', '|', '~'}.

## Return Value
An IOTHUB_MESSAGE_RESULT value indicating the result of setting the property.

