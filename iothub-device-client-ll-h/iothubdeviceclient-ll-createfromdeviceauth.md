---                             
title: "IoTHubDeviceClient_LL_CreateFromDeviceAuth function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubDeviceClient_LL_CreateFromDeviceAuth() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubDeviceClient_LL_CreateFromDeviceAuth()

Creates a IoT Hub client for communication with an existing IoT Hub using the device auth module.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_device_client_ll.h](../iothub-device-client-ll-h.md)"  
```C
IOTHUB_DEVICE_CLIENT_LL_HANDLE IoTHubDeviceClient_LL_CreateFromDeviceAuth(
  const char *                      iothub_uri,
  const char *                      device_id,
  IOTHUB_CLIENT_TRANSPORT_PROVIDER  protocol
);
```

## Parameters
* `iothub_uri` Pointer to an ioThub hostname received in the registration process 

* `device_id` Pointer to the device Id of the device 

* `device_auth_handle` A device auth handle used to generate the connection string 

* `protocol` Function pointer for protocol implementation

## Return Value
A non-NULL IOTHUB_DEVICE_CLIENT_LL_HANDLE value that is used when invoking other functions for IoT Hub client and NULL on failure.

