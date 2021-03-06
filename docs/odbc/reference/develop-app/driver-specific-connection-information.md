---
description: Información de conexión específicos del controlador
title: Información de conexión específica del controlador | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLConnect function [ODBC], driver-specific connection information
- connecting to driver [ODBC], SQLConnect
- SQLDriverConnect function [ODBC], driver specific connection information
- connecting to data source [ODBC], SQLDriverConnect
- connecting to driver [ODBC], SQLDriverConnect
- connecting to data source [ODBC], SQLConnect
- connecting to driver [ODBC], driver-specific information
ms.assetid: 3748758a-f16a-4f3b-9c40-06f2e300704e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f026349b4146a37c680185cdeb1d6e2066665222
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88483038"
---
# <a name="driver-specific-connection-information"></a>Información de conexión específicos del controlador
**SQLConnect** supone que el nombre del origen de datos, el identificador de usuario y la contraseña son suficientes para conectarse a un origen de datos y que el resto de la información de conexión se puede almacenar en el sistema. Este no suele ser el caso. Por ejemplo, un controlador podría necesitar un identificador de usuario y una contraseña para iniciar sesión en un servidor y un identificador de usuario y una contraseña diferentes para iniciar sesión en un DBMS. Dado que **SQLConnect** acepta un identificador de usuario y una contraseña únicos, esto significa que el otro identificador de usuario y la contraseña deben almacenarse con la información del origen de datos en el sistema si se va a usar **SQLConnect** . Se trata de una infracción de seguridad potencial y debe evitarse a menos que la contraseña esté cifrada.  
  
 **SQLDriverConnect** permite al controlador definir una cantidad arbitraria de información de conexión en los pares palabra clave-valor de la cadena de conexión. Por ejemplo, suponga que un controlador requiere un nombre de origen de datos, un identificador de usuario y una contraseña para el servidor, así como un identificador de usuario y una contraseña para el DBMS. Un programa personalizado que utilice siempre el origen de datos XYZ Corp podría solicitar al usuario identificadores y contraseñas, y crear el siguiente conjunto de pares de palabra clave-valor, o *cadena de conexión,* para pasar a **SQLDriverConnect**:  
  
> [!NOTE]  
>  Si se va a conectar a un proveedor de origen de datos que admite la autenticación de Windows, debe especificar `Trusted_Connection=yes` en lugar de la información de ID. de usuario y contraseña en la cadena de conexión.  
  
```  
DSN={MyDataSourceName};UID={MyUserID};PWD={MyServerPassword};UIDDBMS={MyDBMSUserID};PWDDBMS={MyDBMSUserPassword};  
```  
  
 La palabra clave **DSN** (nombre del origen de datos) da nombre al origen de datos, las palabras clave **UID** y **pwd** especifican el identificador de usuario y la contraseña para el servidor, y las palabras clave **UIDDBMS** y **PWDDBMS** especifican el identificador de usuario y la contraseña para el DBMS. Observe que el punto y coma final es opcional. **SQLDriverConnect** analiza esta cadena; usa el nombre del origen de datos XYZ Corp para recuperar información de conexión adicional del sistema, como la dirección del servidor. y inician sesión en el servidor y DBMS con los identificadores de usuario y contraseñas especificados.  
  
 Los pares palabra clave-valor de **SQLDriverConnect** deben cumplir ciertas reglas de sintaxis. Las palabras clave y sus valores no deben contener **[] {} (),;? \* =! @** caracteres. El valor de la palabra clave **DSN** no puede constar solo de espacios en blanco y no debe contener espacios en blanco iniciales. Debido a la gramática del registro, las palabras clave y los nombres de los orígenes de datos no pueden contener el carácter de barra diagonal inversa ( \\ ). No se permiten espacios alrededor del signo igual en el par palabra clave-valor.  
  
 La palabra clave **FILEDSN** se puede usar en una llamada a **SQLDriverConnect** para especificar el nombre de un archivo que contiene información del origen de datos (vea [conectar usando orígenes de datos de archivo](../../../odbc/reference/develop-app/connecting-using-file-data-sources.md), más adelante en esta sección). La palabra clave **SaveFile** se puede usar para especificar el nombre de un archivo. DSN en el que se guardarán los pares palabra clave-valor de una conexión correcta realizada por la llamada a **SQLDriverConnect** . Para obtener más información acerca de los orígenes de datos de archivo, consulte la descripción de la función [SQLDriverConnect](../../../odbc/reference/syntax/sqldriverconnect-function.md) .
