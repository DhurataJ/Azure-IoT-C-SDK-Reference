---                             
title: "enrollmentGroup_deserializeFromJson function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the enrollmentGroup_deserializeFromJson() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# enrollmentGroup_deserializeFromJson()

Deserializes a JSON String representation of an Enrollment Group.

## Syntax

\#include "[azure-iot-sdk-c/provisioning_service_client/inc/prov_service_client/provisioning_sc_models_serializer.h](../provisioning-sc-models-serializer-h.md)"  
```C
ENROLLMENT_GROUP_HANDLE enrollmentGroup_deserializeFromJson(const char *  json_string);
```

## Parameters
* `json_string` A JSON String representing an Enrollment Group.

## Return Value
A non-NULL handle representing an Enrollment Group, and NULL on failure.

