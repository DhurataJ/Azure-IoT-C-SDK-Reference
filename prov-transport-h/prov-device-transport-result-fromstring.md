---                             
title: "PROV_DEVICE_TRANSPORT_RESULT_FromString function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the PROV_DEVICE_TRANSPORT_RESULT_FromString() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# PROV_DEVICE_TRANSPORT_RESULT_FromString()

## Syntax

\#include "[azure-iot-sdk-c/provisioning_client/inc/azure_prov_client/prov_transport.h](../prov-transport-h.md)"  
```C
int PROV_DEVICE_TRANSPORT_RESULT_FromString(
  const char *                  enumAsString,
  PROV_DEVICE_TRANSPORT_RESULT  destination
);
```

