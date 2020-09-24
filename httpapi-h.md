---                             
title: "httpapi.h header file reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the header file reference page for httpapi.h in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# httpapi.h 

This module implements the standard HTTP API used by the C IoT client library.

## Includes

\#include <stddef.h>  
\#include "azure_macro_utils/macro_utils.h"  
\#include "azure_c_shared_utility/httpheaders.h"  
\#include "azure_c_shared_utility/buffer_.h"  
\#include "[umock_c/umock_c_prod.h](umock-c-prod-h.md)"  

## Detailed Description

For example, on the Windows platform the HTTP API code uses WinHTTP and for Linux it uses curl and so forth. HTTPAPI must support HTTPs (HTTP+SSL).

## Functions

Function Name                  | Description                                
--------------------------------|---------------------------------------------
[HTTPAPI_RESULTStrings](./httpapi-h/httpapi-resultstrings.md)            | 
[HTTPAPI_RESULT_FromString](./httpapi-h/httpapi-result-fromstring.md)            | 
[HTTPAPI_REQUEST_TYPEStrings](./httpapi-h/httpapi-request-typestrings.md)            | 
[HTTPAPI_REQUEST_TYPE_FromString](./httpapi-h/httpapi-request-type-fromstring.md)            | 
[HTTPAPI_Init](./httpapi-h/httpapi-init.md)            | Global initialization for the HTTP API component.
[HTTPAPI_Deinit](./httpapi-h/httpapi-deinit.md)            | Free resources allocated in [HTTPAPI_Init](httpapi-h/httpapi-init.md).
[HTTPAPI_CreateConnection](./httpapi-h/httpapi-createconnection.md)            | Creates an HTTPS connection to the host specified by the hostName parameter.
[HTTPAPI_CloseConnection](./httpapi-h/httpapi-closeconnection.md)            | Closes a connection created with [HTTPAPI_CreateConnection](httpapi-h/httpapi-createconnection.md).
[HTTPAPI_ExecuteRequest](./httpapi-h/httpapi-executerequest.md)            | Sends the HTTP request to the host and handles the response for the HTTP call.
[HTTPAPI_SetOption](./httpapi-h/httpapi-setoption.md)            | Sets the option named optionName bearing the value value for the HTTP_HANDLE handle.
[HTTPAPI_CloneOption](./httpapi-h/httpapi-cloneoption.md)            | Clones the option named optionName bearing the value value into the pointer savedValue.

## Macro definitions

#### AMBIGUOUS_STATUS_CODE

```C
#define AMBIGUOUS_STATUS_CODE  (300) 
```

#### HTTPAPI_RESULT_VALUES

```C
#define HTTPAPI_RESULT_VALUES \
        HTTPAPI_OK, \
        HTTPAPI_INVALID_ARG, \
        HTTPAPI_ERROR, \
        HTTPAPI_OPEN_REQUEST_FAILED, \
        HTTPAPI_SET_OPTION_FAILED, \
        HTTPAPI_SEND_REQUEST_FAILED, \
        HTTPAPI_RECEIVE_RESPONSE_FAILED, \
        HTTPAPI_QUERY_HEADERS_FAILED, \
        HTTPAPI_QUERY_DATA_AVAILABLE_FAILED, \
        HTTPAPI_READ_DATA_FAILED, \
        HTTPAPI_ALREADY_INIT, \
        HTTPAPI_NOT_INIT, \
        HTTPAPI_HTTP_HEADERS_FAILED, \
        HTTPAPI_STRING_PROCESSING_ERROR, \
        HTTPAPI_ALLOC_FAILED, \
        HTTPAPI_INIT_FAILED, \
        HTTPAPI_INSUFFICIENT_RESPONSE_BUFFER, \
        HTTPAPI_SET_X509_FAILURE, \
        HTTPAPI_SET_TIMEOUTS_FAILED 
```

#### HTTPAPI_REQUEST_TYPE_VALUES

```C
#define HTTPAPI_REQUEST_TYPE_VALUES \
        HTTPAPI_REQUEST_GET, \
        HTTPAPI_REQUEST_POST, \
        HTTPAPI_REQUEST_PUT, \
        HTTPAPI_REQUEST_DELETE, \
        HTTPAPI_REQUEST_PATCH, \
        HTTPAPI_REQUEST_HEAD 
```

#### MAX_HOSTNAME_LEN

```C
#define MAX_HOSTNAME_LEN  65 
```

#### MAX_USERNAME_LEN

```C
#define MAX_USERNAME_LEN  65 
```

#### MAX_PASSWORD_LEN

```C
#define MAX_PASSWORD_LEN  65 
```

## Enumeration types

#### HTTPAPI_RESULT

Enumeration specifying the possible return values for the APIs in this module. 

```C
enum HTTPAPI_RESULT {
  HTTPAPI_RESULT_INVALID,
  HTTPAPI_OK,
  HTTPAPI_INVALID_ARG,
  HTTPAPI_ERROR,
  HTTPAPI_OPEN_REQUEST_FAILED,
  HTTPAPI_SET_OPTION_FAILED,
  HTTPAPI_SEND_REQUEST_FAILED,
  HTTPAPI_RECEIVE_RESPONSE_FAILED,
  HTTPAPI_QUERY_HEADERS_FAILED,
  HTTPAPI_QUERY_DATA_AVAILABLE_FAILED,
  HTTPAPI_READ_DATA_FAILED,
  HTTPAPI_ALREADY_INIT,
  HTTPAPI_NOT_INIT,
  HTTPAPI_HTTP_HEADERS_FAILED,
  HTTPAPI_STRING_PROCESSING_ERROR,
  HTTPAPI_ALLOC_FAILED,
  HTTPAPI_INIT_FAILED,
  HTTPAPI_INSUFFICIENT_RESPONSE_BUFFER,
  HTTPAPI_SET_X509_FAILURE,
  HTTPAPI_SET_TIMEOUTS_FAILED
}
```

#### HTTPAPI_REQUEST_TYPE

Enumeration specifying the HTTP request verbs accepted by the HTTPAPI module. 

```C
enum HTTPAPI_REQUEST_TYPE {
  HTTPAPI_REQUEST_TYPE_INVALID,
  HTTPAPI_REQUEST_GET,
  HTTPAPI_REQUEST_POST,
  HTTPAPI_REQUEST_PUT,
  HTTPAPI_REQUEST_DELETE,
  HTTPAPI_REQUEST_PATCH,
  HTTPAPI_REQUEST_HEAD
}
```

## Type definitions

#### HTTP_HANDLE

```C
typedef struct HTTP_HANDLE_DATA_TAG* HTTP_HANDLE;
```

