---                             
title: "HTTPAPI_ExecuteRequest function reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the function reference page for the HTTPAPI_ExecuteRequest() function in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 09/23/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# HTTPAPI_ExecuteRequest()

Sends the HTTP request to the host and handles the response for the HTTP call.

## Syntax

\#include "[azure-iot-sdk-c/c-utility/inc/azure_c_shared_utility/httpapi.h](../httpapi-h.md)"  
```C
HTTPAPI_RESULT HTTPAPI_ExecuteRequest(
  HTTP_HANDLE            handle,
  HTTPAPI_REQUEST_TYPE   requestType,
  const char *           relativePath,
  HTTP_HEADERS_HANDLE    httpHeadersHandle,
  const unsigned char *  content,
  size_t                 contentLength,
  unsigned int *         statusCode,
  HTTP_HEADERS_HANDLE    responseHeadersHandle,
  BUFFER_HANDLE          responseContent
);
```

## Parameters
* `handle` The handle to the HTTP connection created via [HTTPAPI_CreateConnection](../httpapi-h/httpapi-createconnection.md). 

* `requestType` Specifies which HTTP method is used (GET, POST, DELETE, PUT, PATCH). 

* `relativePath` Specifies the relative path of the URL excluding the host name. 

* `httpHeadersHandle` Specifies a set of HTTP headers (name-value pairs) to be added to the HTTP request. The httpHeadersHandle handle can be created and setup with the proper name-value pairs by using the HTTPHeaders APIs available in HTTPHeaders.h. 

* `content` Specifies a pointer to the request body. This value is optional and can be NULL. 

* `contentLength` Specifies the request body size (this is typically added into the HTTP headers as the Content-Length header). This value is optional and can be 0. 

* `statusCode` This is an out parameter, where [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) returns the status code from the HTTP response (200, 201, 400, 401, etc.) 

* `responseHeadersHandle` This is an HTTP headers handle to which [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) must add all the HTTP response headers so that the caller of [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) can inspect them. You can manipulate responseHeadersHandle by using the HTTPHeaders APIs available in HTTPHeaders.h

* `responseContent` This is a buffer that must be filled by [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) with the contents of the HTTP response body. The buffer size must be increased by the [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) implementation in order to fit the response body. [HTTPAPI_ExecuteRequest](../httpapi-h/httpapi-executerequest.md) must also handle chunked transfer encoding for HTTP responses. To manipulate the responseContent buffer, use the APIs available in [Strings.h](../strings-h.md).

## Return Value
HTTPAPI_OK if the API call is successful or an error code in case it fails.

