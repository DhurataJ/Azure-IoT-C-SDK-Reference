---                             
title: "IoTHubMessage_SetDiagnosticPropertyData function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessage_SetDiagnosticPropertyData() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessage_SetDiagnosticPropertyData()

Sets the DiagnosticData for the IOTHUB_MESSAGE_HANDLE. CAUTION: SDK user should not call it directly, it is for internal use only.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_message.h](../iothub-message-h.md)"  
```C
IOTHUB_MESSAGE_RESULT IoTHubMessage_SetDiagnosticPropertyData(
  IOTHUB_MESSAGE_HANDLE  iotHubMessageHandle,
  const                  diagnosticData
);
```

## Parameters
* `iotHubMessageHandle` Handle to the message. 

* `diagnosticData` Pointer to the memory location of the diagnosticData

## Return Value
Returns IOTHUB_MESSAGE_OK if the DiagnosticData was set successfully or an error code otherwise.

