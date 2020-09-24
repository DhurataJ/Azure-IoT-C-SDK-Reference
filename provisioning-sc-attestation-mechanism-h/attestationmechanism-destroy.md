---                             
title: "attestationMechanism_destroy function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the attestationMechanism_destroy() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/24/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# attestationMechanism_destroy()

Destroys an Attestation Mechanism handle, freeing all allocated memory. Please note that this also includes any memory in more specific handles generated from the handle (e.g. TPM_ATTESTATION_HANDLE). Please note further that this will also cause any Enrollment that the Attestation Mechanism has been attached to to have unexpected behvaiours. Do not use this function unless the attestation mechanism is unattached.

## Syntax

\#include "[azure-iot-sdk-c/provisioning_service_client/inc/prov_service_client/provisioning_sc_attestation_mechanism.h](../provisioning-sc-attestation-mechanism-h.md)"  
```C
void attestationMechanism_destroy(ATTESTATION_MECHANISM_HANDLE  MU_C2);
```

## Parameters
* `att_mech` The handle of the Attestation Mechanism

