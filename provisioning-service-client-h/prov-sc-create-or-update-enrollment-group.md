---                             
title: "prov_sc_create_or_update_enrollment_group function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the prov_sc_create_or_update_enrollment_group() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# prov_sc_create_or_update_enrollment_group()

Creates or updates a device enrollment group record on the Provisioning Service.

## Syntax

\#include "[azure-iot-sdk-c/provisioning_service_client/inc/prov_service_client/provisioning_service_client.h](../provisioning-service-client-h.md)"  
```C
int prov_sc_create_or_update_enrollment_group(
  PROVISIONING_SERVICE_CLIENT_HANDLE  prov_client,
  ENROLLMENT_GROUP_HANDLE             enrollment_ptr
);
```

## Parameters
* `prov_client` The handle used for connecting to the Provisioning Service. 

* `enrollment_ptr` Pointer to a handle for a new or updated enrollment group.

## Return Value
0 upon success, a non-zero number upon failure.

