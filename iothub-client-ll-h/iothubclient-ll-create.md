---                             
title: "IoTHubClient_LL_Create function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubClient_LL_Create() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubClient_LL_Create()

Creates a IoT Hub client for communication with an existing IoT Hub using the specified parameters.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_client_ll.h](../iothub-client-ll-h.md)"  
```C
IOTHUB_CLIENT_LL_HANDLE IoTHubClient_LL_Create(const   MU_C2);
```

## Parameters
* `config` Pointer to an [IOTHUB_CLIENT_CONFIG](../iothub-client-core-common-h.md#iothub_client_config) structure

The API does not allow sharing of a connection across multiple devices. This is a blocking call.

## Return Value
A non-NULL IOTHUB_CLIENT_LL_HANDLE value that is used when invoking other functions for IoT Hub client and NULL on failure.

