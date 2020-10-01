---                             
title: "iothub_security_set_symmetric_key_info function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the iothub_security_set_symmetric_key_info() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# iothub_security_set_symmetric_key_info()

## Syntax

\#include "[azure-iot-sdk-c/provisioning_client/inc/azure_prov_client/iothub_security_factory.h](../iothub-security-factory-h.md)"  
```C
int iothub_security_set_symmetric_key_info(
  const char *  registration_name,
  const char *  symmetric_key
);
```

