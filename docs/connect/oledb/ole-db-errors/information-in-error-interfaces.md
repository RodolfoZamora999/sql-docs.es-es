---
title: Información en interfaces de error
description: Microsoft OLE DB Driver for SQL Server notifica alguna información de error y estado en las interfaces de error definidas por OLE DB IErrorInfo, IErrorRecords e ISQLErrorInfo.
ms.custom: ''
ms.date: 05/06/2020
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- OLE DB Driver for SQL Server, errors
- IErrorRecords interface
- IErrorInfo interface
- OLE DB error handling, error interfaces
- ISQLErrorInfo interface
- errors [OLE DB], error interfaces
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7651d01bef5b17981c0e4c93c450f26e7970524d
ms.sourcegitcommit: 7eb80038c86acfef1d8e7bfd5f4e30e94aed3a75
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "92081924"
---
# <a name="information-in-error-interfaces"></a>Información en interfaces de error
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  El controlador OLE DB para SQL Server notifica alguna información de error y estado en las interfaces de error definidas por OLE DB **IErrorInfo**, **IErrorRecords** e **ISQLErrorInfo**.  
  
 OLE DB Driver for SQL Server admite las funciones miembro **IErrorInfo**, como se indica a continuación.  
  
|Función de miembro|Descripción|  
|---------------------|-----------------|  
|**GetDescription**|Cadena de mensaje de error descriptiva.|  
|**GetGUID**|GUID de la interfaz que definió el error.|  
|**GetHelpContext**|No compatible. Siempre devuelve cero.|  
|**GetHelpFile**|No compatible. Siempre devuelve NULL.|  
|**GetSource**|Cadena "Controlador Microsoft OLE DB para SQL Server".|  
  
 OLE DB Driver for SQL Server admite funciones miembro **IErrorRecords**, de la manera siguiente.  
  
|Función de miembro|Descripción|  
|---------------------|-----------------|  
|**GetBasicErrorInfo**|Llena una estructura ERRORINFO con información básica acerca de un error. Una estructura ERRORINFO contiene miembros que identifican el valor devuelto HRESULT del error así como el proveedor y la interfaz a los que se aplica el error.|  
|**GetCustomErrorObject**|Devuelve una referencia en las interfaces **ISQLErrorInfo** e [ISQLServerErrorInfo](../ole-db-interfaces/isqlservererrorinfo-geterrorinfo-ole-db.md).|  
|**GetErrorInfo**|Devuelve una referencia en una interfaz **IErrorInfo**.|  
|**GetErrorParameters**|OLE DB Driver for SQL Server no devuelve parámetros al consumidor mediante **GetErrorParameters**.|  
|**GetRecordCount**|Recuento de registros de error disponibles.|  
  
 OLE DB Driver for SQL Server admite parámetros **ISQLErrorInfo::GetSQLInfo**, como se indica a continuación.  
  
|Parámetro|Descripción|  
|---------------|-----------------|  
|*pbstrSQLState*|Devuelve un valor SQLSTATE para el error. Los valores SQLSTATE se definen en las especificaciones SQL 92, ODBC e ISO SQL y API. Ni [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] ni OLE DB Driver for SQL Server han definido valores SQLSTATE específicos de la implementación.|  
|*plNativeError*|Devuelve el número de error de [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] procedente de **master.dbo.sysmessages** cuando está disponible. Están disponibles errores nativos después de un intento correcto de inicializar un origen de datos de OLE DB Driver for SQL Server. Antes del intento, OLE DB Driver for SQL Server siempre devuelve cero.|  
  
## <a name="see-also"></a>Consulte también  
 [Errores](../../oledb/ole-db-errors/errors.md)  
  
