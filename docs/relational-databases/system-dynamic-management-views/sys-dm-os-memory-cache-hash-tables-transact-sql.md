---
description: sys.dm_os_memory_cache_hash_tables (Transact-SQL)
title: Sys. dm_os_memory_cache_hash_tables (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/13/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.dm_os_memory_cache_hash_tables_TSQL
- sys.dm_os_memory_cache_hash_tables
- dm_os_memory_cache_hash_tables
- dm_os_memory_cache_hash_tables_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_os_memory_cache_hash_tables dynamic management view
ms.assetid: 68b94f35-8f80-4d2b-bcde-7a21934219af
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 0013d45519560f6bda0437f2977a1d071dd1b424
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89546552"
---
# <a name="sysdm_os_memory_cache_hash_tables-transact-sql"></a>sys.dm_os_memory_cache_hash_tables (Transact-SQL)
[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Devuelve una fila para cada caché activa en la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].  
  
> [!NOTE]  
>  Para llamar a este método desde [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] o [!INCLUDE[ssPDW](../../includes/sspdw-md.md)] , use el nombre **Sys. dm_pdw_nodes_os_memory_cache_hash_tables**.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**cache_address**|**varbinary(8**|Dirección (clave principal) de la entrada de caché. No admite valores NULL.|  
|**name**|**nvarchar(256)**|Nombre de la caché. No admite valores NULL.|  
|**type**|**nvarchar(60)**|Tipo de caché. No admite valores NULL.|  
|**table_level**|**int**|Número de tabla de hash. Una caché concreta puede tener varias tablas hash que corresponden a diferentes funciones de hash. No admite valores NULL.|  
|**buckets_count**|**int**|Número de depósitos en la tabla de hash. No admite valores NULL.|  
|**buckets_in_use_count**|**int**|Número de depósitos que se utilizan actualmente. No admite valores NULL.|  
|**buckets_min_length**|**int**|Número mínimo de entradas de caché en un depósito. No admite valores NULL.|  
|**buckets_max_length**|**int**|Número máximo de entradas de caché en un depósito. No admite valores NULL.|  
|**buckets_avg_length**|**int**|Número promedio de entradas de caché en cada depósito. No admite valores NULL.|  
|**buckets_max_length_ever**|**int**|Número máximo de entradas de caché en un depósito de hash en esta tabla de hash desde que se inició el servidor. No admite valores NULL.|  
|**hits_count**|**bigint**|Proporción de aciertos de la caché. No admite valores NULL.|  
|**misses_count**|**bigint**|Número de errores de la caché. No admite valores NULL.|  
|**buckets_avg_scan_hit_length**|**int**|Número promedio de entradas examinadas en un depósito antes de haber encontrado la búsqueda de un elemento. No admite valores NULL.|  
|**buckets_avg_scan_miss_length**|**int**|Número promedio de entradas examinadas en un depósito antes de haber finalizado la búsqueda sin éxito. No admite valores NULL.|  
|**pdw_node_id**|**int**|Identificador del nodo en el que se encuentra esta distribución.<br /><br /> **Se aplica a**: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] , [!INCLUDE[ssPDW](../../includes/sspdw-md.md)]|  
  
## <a name="permissions"></a>Permisos 

En [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)] , requiere el `VIEW SERVER STATE` permiso.   
En [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)] los niveles Premium, requiere el `VIEW DATABASE STATE` permiso en la base de datos. En [!INCLUDE[ssSDS_md](../../includes/sssds-md.md)] los niveles estándar y básico, requiere el  **Administrador del servidor** o una cuenta de **Administrador de Azure Active Directory** .   

## <a name="see-also"></a>Consulte también  
 
  [SQL Server vistas de administración dinámica relacionadas con el sistema operativo &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/sql-server-operating-system-related-dynamic-management-views-transact-sql.md)  
  
  


