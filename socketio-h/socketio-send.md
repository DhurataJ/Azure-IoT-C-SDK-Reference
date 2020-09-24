---                             
title: "socketio_send function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the socketio_send() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# socketio_send()

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/socketio.h](../socketio-h.md)"  
```C
int socketio_send(
  CONCRETE_IO_HANDLE  socket_io,
  const void *        buffer,
  size_t              size,
  ON_SEND_COMPLETE    on_send_complete,
  void *              callback_context
);
```

