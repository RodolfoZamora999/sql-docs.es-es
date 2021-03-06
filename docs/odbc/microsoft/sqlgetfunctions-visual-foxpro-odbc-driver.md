---
description: SQLGetFunctions (controlador ODBC de Visual FoxPro)
title: SQLGetFunctions (controlador ODBC de Visual FoxPro) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLGetFunctions function [ODBC], Visual FoxPro ODBC Driver
ms.assetid: 8102932a-88b3-49d8-bf7a-c766f54878c0
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: df1413b657ec4631390525a702a625ba480e9f7e
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88340121"
---
# <a name="sqlgetfunctions-visual-foxpro-odbc-driver"></a>SQLGetFunctions (controlador ODBC de Visual FoxPro)
> [!NOTE]  
>  Este tema contiene información específica del controlador ODBC de Visual FoxPro. Para obtener información general sobre esta función, vea el tema correspondiente en referencia de la [API de ODBC](../../odbc/reference/syntax/odbc-api-reference.md).  
  
 Compatibilidad: completa  
  
 Conformidad con la API de ODBC: nivel 1  
  
 Devuelve TRUE para todas las funciones admitidas.  
  
 El controlador ODBC de Visual FoxPro es compatible con todas las funciones principales y de nivel 1 de la API de ODBC. En la tabla siguiente se indica si el controlador admite una función de nivel 2 específica.  
  
|*Function*|Compatible|  
|----------------|---------------|  
|SQL_API_SQLBROWSECONNECT|No|  
|SQL_API_SQLCOLUMNPRIVELEGES|No|  
|SQL_API_SQLDATASOURCES|Sí|  
|SQL_API_SQLDESCRIBEPARAM|No|  
|SQL_API_SQLDRIVERS|Sí|  
|SQL_API_SQLEXTENDEDFETCH|Sí|  
|SQL_API_SQLFOREIGNKEYS|No|  
|SQL_API_SQLMORERESULTS|Sí|  
|SQL_API_SQLNATIVESQL|No|  
|SQL_API_SQLNUMPARAMS|Sí|  
|SQL_API_SQLPARAMOPTIONS|Sí|  
|SQL_API_SQLPRIMARYKEYS|Sí|  
|SQL_API_SQLPROCEDURECOLUMNS|No|  
|SQL_API_SQLPROCEDURES|No|  
|SQL_API_SQLSETPOS|Sí|  
|SQL_API_SQLSETSCROLLOPTIONS|Sí|  
|SQL_API_SQLTABLEPRIVILEGES|No|  
  
 Para obtener más información, vea [SQLGetFunctions](../../odbc/reference/syntax/sqlgetfunctions-function.md) en la *Referencia del programador de ODBC*.
