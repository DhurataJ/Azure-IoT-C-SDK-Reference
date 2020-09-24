---                             
title: "IoTHubModuleClient_CreateFromConnectionString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubModuleClient_CreateFromConnectionString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubModuleClient_CreateFromConnectionString()

Creates a IoT Hub client for communication with an existing IoT Hub using the specified connection string parameter.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_module_client.h](../iothub-module-client-h.md)"  
```C
IOTHUB_MODULE_CLIENT_HANDLE IoTHubModuleClient_CreateFromConnectionString(
  const char *                      connectionString,
  IOTHUB_CLIENT_TRANSPORT_PROVIDER  protocol
);
```

## Parameters
* `connectionString` Pointer to a character string 

* `protocol` Function pointer for protocol implementation

Sample connection string: 
```
HostName=[IoT Hub name goes here].[IoT Hub suffix goes here, e.g., private.azure-devices-int.net];DeviceId=[Device ID goes here];SharedAccessKey=[Device key goes here];ModuleId=[Module ID goes here]
```

```
HostName=[IoT Hub name goes here].[IoT Hub suffix goes here, e.g., private.azure-devices-int.net];DeviceId=[Device ID goes here];SharedAccessSignature=SharedAccessSignature sr=[IoT Hub name goes here].[IoT Hub suffix goes here, e.g., private.azure-devices-int.net]/devices/[Device ID goes here]&sig=[SAS Token goes here]&se=[Expiry Time goes here];ModuleId=[Module ID goes here]
```

## Return Value
A non-NULL IOTHUB_MODULE_CLIENT_HANDLE value that is used when invoking other functions for IoT Hub client and NULL on failure.

