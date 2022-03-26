---                             
title: "xio_close function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the xio_close() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 03/25/2022                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# xio_close()

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/xio.h](../xio-h.md)"  
```C
int xio_close(
  XIO_HANDLE            xio,
  ON_IO_CLOSE_COMPLETE  on_io_close_complete,
  void *                callback_context
);
```

