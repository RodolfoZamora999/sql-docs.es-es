---
description: Método setTimestamp (java.lang.String, java.sql.Timestamp)
title: Método setTimestamp para el valor de marca de tiempo | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerCallableStatement.setTimestamp (java.lang.String, java.sql.Timestamp)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: dc45b126-3196-47ff-956b-cbc897980ff8
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 9f176b15ac48910cf4ce1de74a284fa5080cbc75
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88450689"
---
# <a name="settimestamp-method-javalangstring-javasqltimestamp"></a>Método setTimestamp (java.lang.String, java.sql.Timestamp)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Establece el parámetro designado para el valor de marca de tiempo determinado.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void setTimestamp(java.lang.String sCol,  
                         java.sql.Timestamp t)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *sCol*  
  
 Objeto **String** que contiene el nombre del parámetro.  
  
 *t*  
  
 Un objeto Timestamp.  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Observaciones  
 El método setTimestamp especifica este método setTimestamp en la interfaz java.sql.CallableStatement.  
  
## <a name="see-also"></a>Consulte también  
 [Método setTimestamp &#40;SQLServerCallableStatement&#41;](../../../connect/jdbc/reference/settimestamp-method-sqlservercallablestatement.md)   
 [Miembros SQLServerCallableStatement](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [Clase SQLServerCallableStatement](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
