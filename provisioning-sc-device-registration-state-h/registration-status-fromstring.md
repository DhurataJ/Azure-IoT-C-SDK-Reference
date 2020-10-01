---                             
title: "REGISTRATION_STATUS_FromString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the REGISTRATION_STATUS_FromString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# REGISTRATION_STATUS_FromString()

## Syntax

\#include "[azure-iot-sdk-c/provisioning_service_client/inc/prov_service_client/provisioning_sc_device_registration_state.h](../provisioning-sc-device-registration-state-h.md)"  
```C
int REGISTRATION_STATUS_FromString(
  const char *         enumAsString,
  REGISTRATION_STATUS  destination
);
```

