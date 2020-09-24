---                             
title: "IoTHubClient_UploadMultipleBlocksToBlobAsync function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the IoTHubClient_UploadMultipleBlocksToBlobAsync() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# IoTHubClient_UploadMultipleBlocksToBlobAsync()

Uploads a file to a Blob storage in chunks, fed through the callback function provided by the user.

## Syntax

\#include "[azure-iot-sdk-c/iothub_client/inc/iothub_client.h](../iothub-client-h.md)"  
```C
IOTHUB_CLIENT_RESULT IoTHubClient_UploadMultipleBlocksToBlobAsync(
  IOTHUB_CLIENT_HANDLE                         iotHubClientHandle,
  const char *                                 destinationFileName,
  IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK  getDataCallback,
  void *                                       context
);
```

DEPRECATED: Use IoTHubClient_UploadMultipleBlocksToBlobAsyncEx instead ** 
## Remarks
This function allows users to upload large files in chunks, not requiring the whole file content to be passed in memory. 

## Parameters
* `iotHubClientHandle` The handle created by a call to the IoTHubClient_Create function. 

* `destinationFileName` The name of the file to be created in Azure Blob Storage. 

* `getDataCallback` A callback to be invoked to acquire the file chunks to be uploaded, as well as to indicate the status of the upload of the previous block. 

* `context` Any data provided by the user to serve as context on getDataCallback. 

## Return Value
An IOTHUB_CLIENT_RESULT value indicating the success or failure of the API call. DEPRECATED: Use IoTHubClient_UploadMultipleBlocksToBlobAsyncEx instead **

