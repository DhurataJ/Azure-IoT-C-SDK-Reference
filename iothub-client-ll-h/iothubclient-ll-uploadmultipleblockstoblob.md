---                             
title: "IoTHubClient_LL_UploadMultipleBlocksToBlob function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubClient_LL_UploadMultipleBlocksToBlob() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubClient_LL_UploadMultipleBlocksToBlob()

This API uploads to Azure Storage the content provided block by block by getDataCallback under the blob name devicename/.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_client_ll.h](../iothub-client-ll-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubClient_LL_UploadMultipleBlocksToBlob(
  IOTHUB_CLIENT_LL_HANDLE                      iotHubClientHandle,
  const char *                                 destinationFileName,
  IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK  getDataCallback,
  void *                                       context
);
```

DEPRECATED: Use IoTHubClient_LL_UploadMultipleBlocksToBlobAsyncEx instead ** 
## Parameters
* `iotHubClientHandle` The handle created by a call to the create function. 

* `destinationFileName` name of the file. 

* `getDataCallback` A callback to be invoked to acquire the file chunks to be uploaded, as well as to indicate the status of the upload of the previous block. 

* `context` Any data provided by the user to serve as context on getDataCallback.

## Return Value
IOTHUB_CLIENT_OK upon success or an error code upon failure. DEPRECATED: Use IoTHubClient_LL_UploadMultipleBlocksToBlobAsyncEx instead **

