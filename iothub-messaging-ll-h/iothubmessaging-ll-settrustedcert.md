---                             
title: "IoTHubMessaging_LL_SetTrustedCert function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubMessaging_LL_SetTrustedCert() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubMessaging_LL_SetTrustedCert()

This function is meant to be called by the user when to set the trusted certificate on the tls connection.

## Syntax

\#include "[azure-iot-sdk-c/iothub_service_client/inc/iothub_messaging_ll.h](../iothub-messaging-ll-h.md)"  
```C
IOTHUB_MESSAGING_RESULT IoTHubMessaging_LL_SetTrustedCert(
  IOTHUB_MESSAGING_HANDLE  messagingHandle,
  const char *             trusted_cert
);
```

## Parameters
* `messagingHandle` The handle created by a call to the create function. 

* `trusted_cert` The trusted certificate that will be set.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

