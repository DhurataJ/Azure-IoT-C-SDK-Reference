---                             
title: "UniqueId_Generate function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the UniqueId_Generate() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# UniqueId_Generate()

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/uniqueid.h](../uniqueid-h.md)"  
```C
UNIQUEID_RESULT UniqueId_Generate(
  char *  uid,
  size_t  bufferSize
);
```

