---
description: Método setTransactionIsolation (SQLServerConnection)
title: Método setTransactionIsolation (SQLServerConnection) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerConnection.setTransactionIsolation
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 6a8fa4d3-5237-40f8-8a02-b40a3d7a1131
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 552920c275dee8b1dede1b229b593ce8b7547428
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88355008"
---
# <a name="settransactionisolation-method-sqlserverconnection"></a>Método setTransactionIsolation (SQLServerConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Intenta cambiar el nivel de aislamiento de transacción para este objeto [SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md) según el que se haya determinado.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void setTransactionIsolation(int level)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *level*  
  
 Un valor **int** que contiene uno de los siguientes niveles de aislamiento:  
  
 TRANSACTION_READ_UNCOMMITTED  
  
 TRANSACTION_READ_COMMITTED  
  
 TRANSACTION_REPEATABLE_READ  
  
 TRANSACTION_SERIALIZABLE  
  
 TRANSACTION_SNAPSHOT = 0x1000  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Observaciones  
 El método setTransactionIsolation especifica este método setTransactionIsolation en la interfaz java.sql.Connection.  
  
 No se confirman las transacciones si se llama a este método durante el transcurso de una transacción.  
  
## <a name="see-also"></a>Consulte también  
 [Miembros SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [Clase SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
