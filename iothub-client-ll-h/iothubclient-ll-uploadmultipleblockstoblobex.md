---                             
title: "IoTHubClient_LL_UploadMultipleBlocksToBlobEx function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubClient_LL_UploadMultipleBlocksToBlobEx() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubClient_LL_UploadMultipleBlocksToBlobEx()

This API uploads to Azure Storage the content provided block by block by getDataCallback under the blob name devicename/.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_client_ll.h](../iothub-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubClient_LL_UploadMultipleBlocksToBlobEx(IOTHUB_CLIENT_LL_HANDLE  MU_IFCOMMA2);
```

## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `destinationFileName` name of the file. 

* `getDataCallbackEx` A callback to be invoked to acquire the file chunks to be uploaded, as well as to indicate the status of the upload of the previous block. 

* `context` Any data provided by the user to serve as context on getDataCallback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure.

