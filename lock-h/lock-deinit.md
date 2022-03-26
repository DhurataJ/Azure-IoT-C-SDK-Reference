---                             
title: "Lock_Deinit function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the Lock_Deinit() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# Lock_Deinit()

The lock instance is destroyed.

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/lock.h](../lock-h.md)"  
```C
LOCK_RESULT Lock_Deinit(LOCK_HANDLE  handle);
```

## Parameters
* `handle` A valid handle to the lock.

## Return Value
Returns LOCK_OK when the lock object has been destroyed and LOCK_ERROR when an error occurs.

