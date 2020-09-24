---                             
title: "prov_sc_delete_enrollment_group_by_param function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the prov_sc_delete_enrollment_group_by_param() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# prov_sc_delete_enrollment_group_by_param()

Deletes a device enrollment group record on the Provisioning Service.

## Syntax

\#include "[azure-iot-sdk-c/provisioning_service_client/inc/prov_service_client/provisioning_service_client.h](../provisioning-service-client-h.md)"  
```C
int prov_sc_delete_enrollment_group_by_param(PROVISIONING_SERVICE_CLIENT_HANDLE  MU_C2);
```

## Parameters
* `prov_client` The handle used for connecting to the Provisioning Service. 

* `group_id` The enrollment group id of the target enrollment group. 

* `etag` The etag of the target enrollment group. If given as "*", will match any etag.

## Return Value
0 upon success, a non-zero number upon failure.

