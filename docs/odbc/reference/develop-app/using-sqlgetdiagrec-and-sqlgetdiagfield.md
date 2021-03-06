---
description: Uso de SQLGetDiagRec y SQLGetDiagField
title: Usar SQLGetDiagRec y SQLGetDiagField | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- diagnostic information [ODBC], SqlGetDiagField
- SQLGetDiagField function [ODBC], and SQLGetDiagRec
- SQLGetDiagRec function [ODBC], and SQLGetDiagField
- diagnostic information [ODBC], SqlGetDiagRec
- retrieving diagnostic information [ODBC]
ms.assetid: 4f486bb1-fad8-4064-ac9d-61f2de85b68b
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 402cb326ac91e13db0d3ab5421bd5ddb097fb3db
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88421439"
---
# <a name="using-sqlgetdiagrec-and-sqlgetdiagfield"></a>Uso de SQLGetDiagRec y SQLGetDiagField
Las aplicaciones llaman a **SQLGetDiagRec** o **SQLGetDiagField** para recuperar información de diagnóstico. Estas funciones aceptan un entorno, una conexión, una instrucción o un identificador de descriptor y devuelven diagnósticos de la función que utilizó por última vez ese identificador. Los diagnósticos registrados en un identificador determinado se descartan cuando se llama a una nueva función mediante ese controlador. Si la función devuelve varios registros de diagnóstico, la aplicación llama a estas funciones varias veces; el número total de registros de estado se recupera mediante una llamada a **SQLGetDiagField** para el registro de encabezado (registro 0) con la opción SQL_DIAG_NUMBER.  
  
 Las aplicaciones recuperan campos de diagnóstico individuales llamando a **SQLGetDiagField** y especificando el campo que se va a recuperar. Algunos campos de diagnóstico no tienen ningún significado para determinados tipos de identificadores. Para obtener una lista de campos de diagnóstico y sus significados, vea la descripción de la función [SQLGetDiagField](../../../odbc/reference/syntax/sqlgetdiagfield-function.md) .  
  
 Las aplicaciones recuperan el SQLSTATE, el código de error nativo y el mensaje de diagnóstico en una sola llamada llamando a **SQLGetDiagRec**; **SQLGetDiagRec** no se puede usar para recuperar información del registro de encabezado.  
  
 Por ejemplo, el código siguiente solicita al usuario una instrucción SQL y la ejecuta. Si se devolvió cualquier información de diagnóstico, llama a **SQLGetDiagField** para obtener el número de registros de estado y **SQLGetDiagRec** para obtener el SQLSTATE, el código de error nativo y el mensaje de diagnóstico de esos registros.  
  
```  
SQLCHAR       SqlState[6], SQLStmt[100], Msg[SQL_MAX_MESSAGE_LENGTH];  
SQLINTEGER    NativeError;  
SQLSMALLINT   i, MsgLen;  
SQLRETURN     rc1, rc2;  
SQLHSTMT      hstmt;  
  
// Prompt the user for an SQL statement.  
GetSQLStmt(SQLStmt);  
  
// Execute the SQL statement and return any errors or warnings.  
rc1 = SQLExecDirect(hstmt, SQLStmt, SQL_NTS);  
if ((rc1 == SQL_SUCCESS_WITH_INFO) || (rc1 == SQL_ERROR)) {
   SQLLEN numRecs = 0;
   SQLGetDiagField(SQL_HANDLE_STMT, hstmt, 0, SQL_DIAG_NUMBER, &numRecs, 0, 0);
   // Get the status records.
   i = 1;  
   while (i <= numRecs && (rc2 = SQLGetDiagRec(SQL_HANDLE_STMT, hstmt, i, SqlState, &NativeError,  
            Msg, sizeof(Msg), &MsgLen)) != SQL_NO_DATA) {  
      DisplayError(SqlState,NativeError,Msg,MsgLen);  
      i++;  
   }  
}  
  
if ((rc1 == SQL_SUCCESS) || (rc1 == SQL_SUCCESS_WITH_INFO)) {  
   // Process statement results, if any.  
}  
```
