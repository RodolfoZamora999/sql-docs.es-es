---
description: Método truncate (SQLServerNClob)
title: Método truncate (SQLServerNClob) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: b7e8210d-a724-4bae-832a-ae4c63031c9c
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 57f75b7b7dea68d6ace682fa2b071f34a2fa1320
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88431497"
---
# <a name="truncate-method-sqlservernclob"></a>Método truncate (SQLServerNClob)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Trunca el valor **NCLOB** según la longitud especificada.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void truncate(long len)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *len*  
  
 La longitud, en caracteres, según la que se debería truncar el valor **NCLOB**.  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Observaciones  
 El método truncate especifica este método truncate en la interfaz java.sql.NClob.  
  
## <a name="see-also"></a>Consulte también  
 [Métodos SQLServerNClob](../../../connect/jdbc/reference/sqlservernclob-methods.md)   
 [Miembros SQLServerNClob](../../../connect/jdbc/reference/sqlservernclob-members.md)   
 [Clase SQLServerNClob](../../../connect/jdbc/reference/sqlservernclob-class.md)  
  
  
