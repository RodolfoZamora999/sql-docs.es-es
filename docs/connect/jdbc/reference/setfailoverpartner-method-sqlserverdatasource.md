---
description: Método setFailoverPartner (SQLServerDataSource)
title: Método setFailoverPartner (SQLServerDataSource) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerDataSource.setFailoverPartner
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 5310b7c2-9d10-474f-ad3a-218fe5da694b
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: c90a6cd4850ad746bafde4646cd459fbcff3e825
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88431887"
---
# <a name="setfailoverpartner-method-sqlserverdatasource"></a>Método setFailoverPartner (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Establece el nombre del servidor de conmutación por error que se usa en la configuración de la creación de reflejo de la base de datos.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public void setFailoverPartner(java.lang.String serverName)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *serverName*  
  
 Unvalor de **String** que contiene el nombre de servidor de conmutación por error.  
  
## <a name="remarks"></a>Observaciones  
 El valor que establece este método se utiliza en caso de que se produzca un error en la conexión inicial con el servidor principal; una vez se haya establecido la conexión inicial, se ignora el valor. El método [setDatabaseName](../../../connect/jdbc/reference/setdatabasename-method-sqlserverdatasource.md) también se debería utilizar junto con este método o se producirá una excepción.  
  
 El controlador no admite especificar el número de puerto del servidor de conmutación por error cuando se establece el nombre de servidor de conmutación por error. Sin embargo, se admite llamar al método [setServerName](../../../connect/jdbc/reference/setservername-method-sqlserverdatasource.md) y al método [setInstanceName](../../../connect/jdbc/reference/setinstancename-method-sqlserverdatasource.md) con el método [setFailoverPartner](../../../connect/jdbc/reference/setfailoverpartner-method-sqlserverdatasource.md).  
  
## <a name="see-also"></a>Consulte también  
 [Miembros SQLServerDataSource](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [Clase SQLServerDataSource](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
