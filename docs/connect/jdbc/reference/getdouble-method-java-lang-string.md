---
description: Método getDouble (java.lang.String)
title: Método getDouble (java.lang.String) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerCallableStatement.getDouble (java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 8eab6a8e-91f3-47b1-8707-5e57368ad0c6
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 61d1dfc94c213c0a982c48f4f9ff665022da390e
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88436177"
---
# <a name="getdouble-method-javalangstring"></a>Método getDouble (java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Recupera el valor del parámetro designado como un objeto **double** en el lenguaje de programación Java según el nombre del parámetro.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public double getDouble(java.lang.String sCol)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *sCol*  
  
 Objeto **String** que contiene el nombre del parámetro.  
  
## <a name="return-value"></a>Valor devuelto  
 Un valor **double**.  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Observaciones  
 El método getDouble especifica este método getDouble en la interfaz java.sql.CallableStatement.  
  
 Este método devuelve todos los tipos de datos basados en número con fidelidad **double** de Java.  
  
## <a name="see-also"></a>Consulte también  
 [Método getDouble &#40;SQLServerCallableStatement&#41;](../../../connect/jdbc/reference/getdouble-method-sqlservercallablestatement.md)   
 [Miembros SQLServerCallableStatement](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [Clase SQLServerCallableStatement](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
