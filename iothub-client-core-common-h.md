---                             
title: "iothub_client_core_common.h header file reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the header file reference page for iothub_client_core_common.h in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# iothub_client_core_common.h 

## Includes

\#include "azure_macro_utils/macro_utils.h"  
\#include "[umock_c/umock_c_prod.h](umock-c-prod-h.md)"  
\#include "[iothub_transport_ll.h](iothub-transport-ll-h.md)"  
\#include "[iothub_message.h](iothub-message-h.md)"  

## Detailed Description

## Functions

Function Name                  | Description                                
--------------------------------|---------------------------------------------
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration specifying the status of calls to various APIs in this module.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration passed in by the IoT Hub when the event confirmation callback is invoked to indicate status of the event processing in the hub.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration returned by the ::IoTHubClient_LL_GetSendStatus API to indicate the current sending status of the IoT Hub client.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | 
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | 
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration returned by the callback which is invoked whenever the IoT Hub sends a message to the device.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration returned by remotely executed functions.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration passed in by the IoT Hub when the event confirmation callback is invoked to indicate status of the event processing in the hub.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration passed in by the IoT Hub when the connection status callback is invoked to indicate status of the connection in the hub.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | Enumeration passed in by the IoT Hub when the connection status callback is invoked to indicate status of the connection in the hub.
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | 
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | 
[MU_DEFINE_ENUM_WITHOUT_INVALID](./iothub-client-core-common-h/mu-define-enum-without-invalid.md)            | 

## Structures

#### IOTHUB_CLIENT_CONFIG

This struct captures IoTHub client configuration.

```C
struct IOTHUB_CLIENT_CONFIG {
  IOTHUB_CLIENT_TRANSPORT_PROVIDER  protocol,
  const char *                      deviceId,
  const char *                      deviceKey,
  const char *                      deviceSasToken,
  const char *                      iotHubName,
  const char *                      iotHubSuffix,
  const char *                      protocolGatewayHostName
};
```
Member name                 | Description                                
----------------------------|----------------
 protocol            | A function pointer that is passed into the IoTHubClientCreate. A function definition for AMQP is defined in the include [iothubtransportamqp.h](iothubtransportamqp-h.md). A function definition for HTTP is defined in the include [iothubtransporthttp.h](iothubtransporthttp-h.md) A function definition for MQTT is defined in the include [iothubtransportmqtt.h](iothubtransportmqtt-h.md).
 deviceId            | A string that identifies the device.
 deviceKey            | The device key used to authenticate the device. If neither deviceSasToken nor deviceKey is present then the authentication is assumed x509.
 deviceSasToken            | The device SAS Token used to authenticate the device in place of device key. If neither deviceSasToken nor deviceKey is present then the authentication is assumed x509.
 iotHubName            | The IoT Hub name to which the device is connecting.
 iotHubSuffix            | IoT Hub suffix goes here, e.g., private.azure-devices-int.net.
 protocolGatewayHostName            | 
#### IOTHUB_CLIENT_DEVICE_CONFIG

This struct captures IoTHub client device configuration.

```C
struct IOTHUB_CLIENT_DEVICE_CONFIG {
  IOTHUB_CLIENT_TRANSPORT_PROVIDER  protocol,
  void *                            transportHandle,
  const char *                      deviceId,
  const char *                      deviceKey,
  const char *                      deviceSasToken
};
```
Member name                 | Description                                
----------------------------|----------------
 protocol            | A function pointer that is passed into the IoTHubClientCreate. A function definition for AMQP is defined in the include [iothubtransportamqp.h](iothubtransportamqp-h.md). A function definition for HTTP is defined in the include [iothubtransporthttp.h](iothubtransporthttp-h.md) A function definition for MQTT is defined in the include [iothubtransportmqtt.h](iothubtransportmqtt-h.md).
 transportHandle            | a transport handle implementing the protocol
 deviceId            | A string that identifies the device.
 deviceKey            | The device key used to authenticate the device. x509 authentication is is not supported for multiplexed connections.
 deviceSasToken            | The device SAS Token used to authenticate the device in place of device key. x509 authentication is is not supported for multiplexed connections.

## Macro definitions

#### IOTHUB_CLIENT_FILE_UPLOAD_RESULT_VALUES

```C
#define IOTHUB_CLIENT_FILE_UPLOAD_RESULT_VALUES  FILE_UPLOAD_OK, \
    FILE_UPLOAD_ERROR 
```

#### IOTHUB_CLIENT_RESULT_VALUES

```C
#define IOTHUB_CLIENT_RESULT_VALUES  IOTHUB_CLIENT_OK,                     \
    IOTHUB_CLIENT_INVALID_ARG,            \
    IOTHUB_CLIENT_ERROR,                  \
    IOTHUB_CLIENT_INVALID_SIZE,           \
    IOTHUB_CLIENT_INDEFINITE_TIME 
```

#### IOTHUB_CLIENT_RETRY_POLICY_VALUES

```C
#define IOTHUB_CLIENT_RETRY_POLICY_VALUES  IOTHUB_CLIENT_RETRY_NONE,                   \
    IOTHUB_CLIENT_RETRY_IMMEDIATE,                  \
    IOTHUB_CLIENT_RETRY_INTERVAL,      \
    IOTHUB_CLIENT_RETRY_LINEAR_BACKOFF,      \
    IOTHUB_CLIENT_RETRY_EXPONENTIAL_BACKOFF,                 \
    IOTHUB_CLIENT_RETRY_EXPONENTIAL_BACKOFF_WITH_JITTER,                 \
    IOTHUB_CLIENT_RETRY_RANDOM 
```

#### IOTHUB_CLIENT_STATUS_VALUES

```C
#define IOTHUB_CLIENT_STATUS_VALUES  IOTHUB_CLIENT_SEND_STATUS_IDLE,       \
    IOTHUB_CLIENT_SEND_STATUS_BUSY 
```

#### IOTHUB_IDENTITY_TYPE_VALUE

```C
#define IOTHUB_IDENTITY_TYPE_VALUE  IOTHUB_TYPE_TELEMETRY,          \
    IOTHUB_TYPE_DEVICE_TWIN,        \
    IOTHUB_TYPE_DEVICE_METHODS,     \
    IOTHUB_TYPE_EVENT_QUEUE 
```

#### IOTHUB_PROCESS_ITEM_RESULT_VALUE

```C
#define IOTHUB_PROCESS_ITEM_RESULT_VALUE  IOTHUB_PROCESS_OK,                      \
    IOTHUB_PROCESS_ERROR,                   \
    IOTHUB_PROCESS_NOT_CONNECTED,           \
    IOTHUB_PROCESS_CONTINUE 
```

#### IOTHUBMESSAGE_DISPOSITION_RESULT_VALUES

```C
#define IOTHUBMESSAGE_DISPOSITION_RESULT_VALUES  IOTHUBMESSAGE_ACCEPTED, \
    IOTHUBMESSAGE_REJECTED, \
    IOTHUBMESSAGE_ABANDONED 
```

#### IOTHUB_CLIENT_IOTHUB_METHOD_STATUS_VALUES

```C
#define IOTHUB_CLIENT_IOTHUB_METHOD_STATUS_VALUES  IOTHUB_CLIENT_IOTHUB_METHOD_STATUS_SUCCESS,   \
    IOTHUB_CLIENT_IOTHUB_METHOD_STATUS_ERROR      \ 
```

#### IOTHUB_CLIENT_CONFIRMATION_RESULT_VALUES

```C
#define IOTHUB_CLIENT_CONFIRMATION_RESULT_VALUES  IOTHUB_CLIENT_CONFIRMATION_OK,                   \
    IOTHUB_CLIENT_CONFIRMATION_BECAUSE_DESTROY,      \
    IOTHUB_CLIENT_CONFIRMATION_MESSAGE_TIMEOUT,      \
    IOTHUB_CLIENT_CONFIRMATION_ERROR                 \ 
```

#### IOTHUB_CLIENT_CONNECTION_STATUS_VALUES

```C
#define IOTHUB_CLIENT_CONNECTION_STATUS_VALUES  IOTHUB_CLIENT_CONNECTION_AUTHENTICATED,                \
    IOTHUB_CLIENT_CONNECTION_UNAUTHENTICATED               \ 
```

#### IOTHUB_CLIENT_CONNECTION_STATUS_REASON_VALUES

```C
#define IOTHUB_CLIENT_CONNECTION_STATUS_REASON_VALUES  IOTHUB_CLIENT_CONNECTION_EXPIRED_SAS_TOKEN,            \
    IOTHUB_CLIENT_CONNECTION_DEVICE_DISABLED,              \
    IOTHUB_CLIENT_CONNECTION_BAD_CREDENTIAL,               \
    IOTHUB_CLIENT_CONNECTION_RETRY_EXPIRED,                \
    IOTHUB_CLIENT_CONNECTION_NO_NETWORK,                   \
    IOTHUB_CLIENT_CONNECTION_COMMUNICATION_ERROR,          \
    IOTHUB_CLIENT_CONNECTION_OK,                           \
    IOTHUB_CLIENT_CONNECTION_NO_PING_RESPONSE              \ 
```

#### TRANSPORT_TYPE_VALUES

```C
#define TRANSPORT_TYPE_VALUES  TRANSPORT_LL, /*LL comes from "LowLevel" */ \
    TRANSPORT_THREADED 
```

#### DEVICE_TWIN_UPDATE_STATE_VALUES

```C
#define DEVICE_TWIN_UPDATE_STATE_VALUES  DEVICE_TWIN_UPDATE_COMPLETE, \
    DEVICE_TWIN_UPDATE_PARTIAL 
```

#### IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_RESULT_VALUES

```C
#define IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_RESULT_VALUES  IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_OK, \
    IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_ABORT 
```

## Type definitions

#### IOTHUB_CLIENT_FILE_UPLOAD_CALLBACK

```C
typedef void(* IOTHUB_CLIENT_FILE_UPLOAD_CALLBACK) (
  IOTHUB_CLIENT_FILE_UPLOAD_RESULT  result,
  void *                            userContextCallback
);
```

#### IOTHUB_METHOD_INVOKE_CALLBACK

```C
typedef void(* IOTHUB_METHOD_INVOKE_CALLBACK) (
  IOTHUB_CLIENT_RESULT  result,
  int                   responseStatus,
  unsigned char *       responsePayload,
  size_t                responsePayloadSize,
  void *                context
);
```

#### IOTHUBTRANSPORT_CONFIG

```C
typedef struct IOTHUBTRANSPORT_CONFIG_TAG IOTHUBTRANSPORT_CONFIG;
```

#### IOTHUB_CLIENT_EVENT_CONFIRMATION_CALLBACK

```C
typedef void(* IOTHUB_CLIENT_EVENT_CONFIRMATION_CALLBACK) (
  IOTHUB_CLIENT_CONFIRMATION_RESULT  result,
  void *                             userContextCallback
);
```

#### IOTHUB_CLIENT_CONNECTION_STATUS_CALLBACK

```C
typedef void(* IOTHUB_CLIENT_CONNECTION_STATUS_CALLBACK) (
  IOTHUB_CLIENT_CONNECTION_STATUS         result,
  IOTHUB_CLIENT_CONNECTION_STATUS_REASON  reason,
  void *                                  userContextCallback
);
```

#### IOTHUB_CLIENT_MESSAGE_CALLBACK_ASYNC

```C
typedef IOTHUBMESSAGE_DISPOSITION_RESULT(* IOTHUB_CLIENT_MESSAGE_CALLBACK_ASYNC) (
  IOTHUB_MESSAGE_HANDLE  message,
  void *                 userContextCallback
);
```

#### IOTHUB_CLIENT_DEVICE_TWIN_CALLBACK

```C
typedef void(* IOTHUB_CLIENT_DEVICE_TWIN_CALLBACK) (
  DEVICE_TWIN_UPDATE_STATE  update_state,
  const unsigned char *     payLoad,
  size_t                    size,
  void *                    userContextCallback
);
```

#### IOTHUB_CLIENT_REPORTED_STATE_CALLBACK

```C
typedef void(* IOTHUB_CLIENT_REPORTED_STATE_CALLBACK) (
  int     status_code,
  void *  userContextCallback
);
```

#### IOTHUB_CLIENT_DEVICE_METHOD_CALLBACK_ASYNC

```C
typedef int(* IOTHUB_CLIENT_DEVICE_METHOD_CALLBACK_ASYNC) (
  const char *           method_name,
  const unsigned char *  payload,
  size_t                 size,
  unsigned char **       response,
  size_t *               response_size,
  void *                 userContextCallback
);
```

#### IOTHUB_CLIENT_INBOUND_DEVICE_METHOD_CALLBACK

```C
typedef int(* IOTHUB_CLIENT_INBOUND_DEVICE_METHOD_CALLBACK) (
  const char *           method_name,
  const unsigned char *  payload,
  size_t                 size,
  METHOD_HANDLE          method_id,
  void *                 userContextCallback
);
```

#### IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK

Callback invoked by IoTHubClient_UploadMultipleBlocksToBlobAsync requesting the chunks of data to be uploaded. 

```C
typedef void(* IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK) (
  IOTHUB_CLIENT_FILE_UPLOAD_RESULT  result,
  unsigned char const **            data,
  size_t *                          size,
  void *                            context
);
```

**Parameters**:

* `result` The result of the upload of the previous block of data provided by the user (IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK_EX only) 

* `data` Next block of data to be uploaded, to be provided by the user when this callback is invoked. 

* `size` Size of the data parameter. 

* `context` User context provided on the call to IoTHubClient_UploadMultipleBlocksToBlobAsync. 

**Remarks**:

If the user wants to abort the upload, the callback should return IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_ABORT It should return IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_OK otherwise. If a NULL is provided for parameter "data" and/or zero is provided for "size", the user indicates to the client that the complete file has been uploaded. In such case this callback will be invoked only once more to indicate the status of the final block upload. If result is not FILE_UPLOAD_OK, the upload is cancelled and this callback stops being invoked. When this callback is called for the last time, no data or size is expected, so data and size are NULL 

#### IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK_EX

```C
typedef IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_RESULT(* IOTHUB_CLIENT_FILE_UPLOAD_GET_DATA_CALLBACK_EX) (
  IOTHUB_CLIENT_FILE_UPLOAD_RESULT  result,
  unsigned char const **            data,
  size_t *                          size,
  void *                            context
);
```

