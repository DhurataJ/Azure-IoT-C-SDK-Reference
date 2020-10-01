---                             
title: "iothub_module_client_ll.h header file reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the header file reference page for iothub_module_client_ll.h in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# iothub_module_client_ll.h 

APIs that allow a user (usually a module) to communicate with an Azure IoTHub.

## Includes

\#include <time.h>  
\#include "azure_macro_utils/macro_utils.h"  
\#include "[umock_c/umock_c_prod.h](umock-c-prod-h.md)"  
\#include "[iothub_transport_ll.h](iothub-transport-ll-h.md)"  
\#include "[iothub_client_core_common.h](iothub-client-core-common-h.md)"  
\#include <stddef.h>  
\#include <stdint.h>  

## Detailed Description

IoTHubModuleClient_LL is a module that allows a user (usually a module) to communicate with an Azure IoTHub. It can send events and receive messages. At any given moment in time there can only be at most 1 message callback function.

This API surface contains a set of APIs that allows the user to interact with the lower layer portion of the IoTHubClient. These APIs contain _LL_ in their name, but retain the same functionality like the IoTHubModuleClient_... APIs, with one difference. If the _LL_ APIs are used then the user is responsible for scheduling when the actual work done by the IoTHubClient happens (when the data is sent/received on/from the wire). This is useful for constrained devices where spinning a separate thread is often not desired.

## Functions

Function Name                  | Description                                
--------------------------------|---------------------------------------------
[IoTHubModuleClient_LL_CreateFromConnectionString](./iothub-module-client-ll-h/iothubmoduleclient-ll-createfromconnectionstring.md)            | Creates a IoT Hub client for communication with an existing IoT Hub using the specified connection string parameter.
[IoTHubModuleClient_LL_Destroy](./iothub-module-client-ll-h/iothubmoduleclient-ll-destroy.md)            | Disposes of resources allocated by the IoT Hub client. This is a blocking call.
[IoTHubModuleClient_LL_SendEventAsync](./iothub-module-client-ll-h/iothubmoduleclient-ll-sendeventasync.md)            | Asynchronous call to send the message specified by eventMessageHandle.
[IoTHubModuleClient_LL_GetSendStatus](./iothub-module-client-ll-h/iothubmoduleclient-ll-getsendstatus.md)            | This function returns the current sending status for IoTHubClient.
[IoTHubModuleClient_LL_SetMessageCallback](./iothub-module-client-ll-h/iothubmoduleclient-ll-setmessagecallback.md)            | Sets up the message callback to be invoked when Edge issues a message to the module. This is a blocking call.
[IoTHubModuleClient_LL_SetConnectionStatusCallback](./iothub-module-client-ll-h/iothubmoduleclient-ll-setconnectionstatuscallback.md)            | Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.
[IoTHubModuleClient_LL_SetRetryPolicy](./iothub-module-client-ll-h/iothubmoduleclient-ll-setretrypolicy.md)            | Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.
[IoTHubModuleClient_LL_GetRetryPolicy](./iothub-module-client-ll-h/iothubmoduleclient-ll-getretrypolicy.md)            | Sets up the connection status callback to be invoked representing the status of the connection to IOT Hub. This is a blocking call.
[IoTHubModuleClient_LL_GetLastMessageReceiveTime](./iothub-module-client-ll-h/iothubmoduleclient-ll-getlastmessagereceivetime.md)            | This function returns in the out parameter lastMessageReceiveTime what was the value of the time function when the last message was received at the client.
[IoTHubModuleClient_LL_DoWork](./iothub-module-client-ll-h/iothubmoduleclient-ll-dowork.md)            | This function is meant to be called by the user when work (sending/receiving) can be done by the IoTHubClient.
[IoTHubModuleClient_LL_SetOption](./iothub-module-client-ll-h/iothubmoduleclient-ll-setoption.md)            | This API sets a runtime option identified by parameter optionName to a value pointed to by value. optionName and the data type value is pointing to are specific for every option.
[IoTHubModuleClient_LL_SetModuleTwinCallback](./iothub-module-client-ll-h/iothubmoduleclient-ll-setmoduletwincallback.md)            | This API specifies a call back to be used when the module receives a desired state update.
[IoTHubModuleClient_LL_SendReportedState](./iothub-module-client-ll-h/iothubmoduleclient-ll-sendreportedstate.md)            | This API sneds a report of the module's properties and their current values.
[IoTHubModuleClient_LL_GetTwinAsync](./iothub-module-client-ll-h/iothubmoduleclient-ll-gettwinasync.md)            | This API enabled the device to request the full module twin (with all the desired and reported properties) on demand.
[IoTHubModuleClient_LL_SetModuleMethodCallback](./iothub-module-client-ll-h/iothubmoduleclient-ll-setmodulemethodcallback.md)            | This API sets callback for async cloud to module method call.
[IoTHubModuleClient_LL_SendEventToOutputAsync](./iothub-module-client-ll-h/iothubmoduleclient-ll-sendeventtooutputasync.md)            | Asynchronous call to send the message specified by eventMessageHandle.
[IoTHubModuleClient_LL_SetInputMessageCallback](./iothub-module-client-ll-h/iothubmoduleclient-ll-setinputmessagecallback.md)            | This API sets callback for method call that is directed to specified 'inputName' queue (e.g. messages from IoTHubClient_SendEventToOutputAsync)

## Type definitions

#### IOTHUB_MODULE_CLIENT_LL_HANDLE

```C
typedef struct IOTHUB_MODULE_CLIENT_LL_HANDLE_DATA_TAG* IOTHUB_MODULE_CLIENT_LL_HANDLE;
```

