---                             
title: "IoTHubDeviceTwin_Create function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceTwin_Create() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceTwin_Create()

Creates a IoT Hub Service Client DeviceTwin handle for use it in consequent APIs.

## Syntax

\#include "[azure-iot-sdk-c/iothub_service_client/inc/iothub_devicetwin.h](../iothub-devicetwin-h.md)"  
```C
IOTHUB_SERVICE_CLIENT_DEVICE_TWIN_HANDLE IoTHubDeviceTwin_Create(IOTHUB_SERVICE_CLIENT_AUTH_HANDLE  serviceClientHandle);
```

## Parameters
* `serviceClientHandle` Service client handle.

## Return Value
A non-NULL IOTHUB_SERVICE_CLIENT_DEVICE_TWIN_HANDLE value that is used when invoking other functions for IoT Hub DeviceTwin and NULL on failure.

