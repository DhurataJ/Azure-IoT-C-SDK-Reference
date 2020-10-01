---                             
title: "IO_SEND_RESULT_FromString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IO_SEND_RESULT_FromString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IO_SEND_RESULT_FromString()

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/xio.h](../xio-h.md)"  
```C
int IO_SEND_RESULT_FromString(
  const char *    enumAsString,
  IO_SEND_RESULT  destination
);
```

