---                             
title: "PLATFORM_INFO_OPTION_FromString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the PLATFORM_INFO_OPTION_FromString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# PLATFORM_INFO_OPTION_FromString()

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/platform.h](../platform-h.md)"  
```C
int PLATFORM_INFO_OPTION_FromString(
  const char *          enumAsString,
  PLATFORM_INFO_OPTION  destination
);
```

