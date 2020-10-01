---                             
title: "map.h header file reference | Microsoft Docs" 
titleSuffix: "Azure IoT C SDK"            
description: "This is the header file reference page for map.h in the Azure IoT C SDK. This SDK is used with Azure IoT Hub and Azure IoT Hub Device Provisioning Service"            
manager: timlt                 
author: wesmc7777              
ms.author: wesmc               
ms.date: 10/01/2020                    
ms.service: "iot-hub"             
ms.custom: ""                
ms.topic: "reference"        
---                            

# map.h 

Map is a module that implements a dictionary of STRING_HANDLE keys to STRING_HANDLE values.

## Includes

\#include <stddef.h>  
\#include "azure_macro_utils/macro_utils.h"  
\#include "[azure_c_shared_utility/strings.h](strings-h.md)"  
\#include "azure_c_shared_utility/crt_abstractions.h"  
\#include "[umock_c/umock_c_prod.h](umock-c-prod-h.md)"  

## Detailed Description

## Functions

Function Name                  | Description                                
--------------------------------|---------------------------------------------
[MAP_RESULTStrings](./map-h/map-resultstrings.md)            | 
[MAP_RESULT_FromString](./map-h/map-result-fromstring.md)            | 
[Map_Create](./map-h/map-create.md)            | Creates a new, empty map.
[Map_Destroy](./map-h/map-destroy.md)            | Release all resources associated with the map.
[Map_Clone](./map-h/map-clone.md)            | Creates a copy of the map indicated by handle and returns a handle to it.
[Map_Add](./map-h/map-add.md)            | Adds a key/value pair to the map.
[Map_AddOrUpdate](./map-h/map-addorupdate.md)            | Adds/updates a key/value pair to the map.
[Map_Delete](./map-h/map-delete.md)            | Removes a key and its associated value from the map.
[Map_ContainsKey](./map-h/map-containskey.md)            | This function returns a boolean value in keyExists if the map contains a key with the same value the parameter key.
[Map_ContainsValue](./map-h/map-containsvalue.md)            | This function returns true in valueExists if at least one <key,value> pair exists in the map where the entry's value is equal to the parameter value.
[Map_GetValueFromKey](./map-h/map-getvaluefromkey.md)            | Retrieves the value of a stored key.
[Map_GetInternals](./map-h/map-getinternals.md)            | Retrieves the complete list of keys and values from the map in values and keys. Also writes the size of the list in count.
[Map_ToJSON](./map-h/map-tojson.md)            | 

## Macro definitions

#### MAP_RESULT_VALUES

```C
#define MAP_RESULT_VALUES \
        MAP_OK, \
        MAP_ERROR, \
        MAP_INVALIDARG, \
        MAP_KEYEXISTS, \
        MAP_KEYNOTFOUND, \
        MAP_FILTER_REJECT 
```

## Enumeration types

#### MAP_RESULT

Enumeration specifying the status of calls to various APIs in this module. 

```C
enum MAP_RESULT {
  MAP_RESULT_INVALID,
  MAP_OK,
  MAP_ERROR,
  MAP_INVALIDARG,
  MAP_KEYEXISTS,
  MAP_KEYNOTFOUND,
  MAP_FILTER_REJECT
}
```

## Type definitions

#### MAP_HANDLE

```C
typedef struct MAP_HANDLE_DATA_TAG* MAP_HANDLE;
```

#### MAP_FILTER_CALLBACK

```C
typedef int(* MAP_FILTER_CALLBACK) (
  const char *  mapProperty,
  const char *  mapValue
);
```

