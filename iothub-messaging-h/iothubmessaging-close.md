---                             
title: "IoTHubMessaging_Close function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessaging_Close() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessaging_Close()

Closes connection to IoTHub.

## Syntax

\#include "[azure-iot-sdk-c/iothub_service_client/inc/iothub_messaging.h](../iothub-messaging-h.md)"  
```C
void IoTHubMessaging_Close(IOTHUB_MESSAGING_CLIENT_HANDLE  MU_IFCOMMA2);
```

## Parameters
* `messagingClientHandle` The handle created by a call to the create function.

