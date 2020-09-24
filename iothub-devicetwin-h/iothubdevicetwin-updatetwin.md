---                             
title: "IoTHubDeviceTwin_UpdateTwin function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceTwin_UpdateTwin() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceTwin_UpdateTwin()

Updates (partial update) the given device's twin info.

## Syntax

\#include "[azure-iot-sdk-c/iothub_service_client/inc/iothub_devicetwin.h](../iothub-devicetwin-h.md)"  
```C
char* IoTHubDeviceTwin_UpdateTwin(IOTHUB_SERVICE_CLIENT_DEVICE_TWIN_HANDLE  MU_C2);
```

## Parameters
* `serviceClientDeviceTwinHandle` The handle created by a call to the create function. 

* `deviceId` The device name (id) to update the twin info for. 

* `deviceTwinJson` DeviceTwin JSon string containing the info (tags, desired properties) to update. All well-known read-only members are ignored. Properties provided with value of null are removed from twin's document.

## Return Value
A non-NULL char* containing updated device twin info upon success or NULL upon failure.

