---
description: sys.trace_columns (Transact-SQL)
title: Sys. trace_columns (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.trace_columns
- trace_columns
- trace_columns_TSQL
- sys.trace_columns_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.trace_columns catalog view
ms.assetid: 5c48eb09-9e9b-45dd-b151-ca39b026ece5
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 1475fdaee1e96ecb5a9498a135bc65109ececf05
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89544980"
---
# <a name="systrace_columns-transact-sql"></a>sys.trace_columns (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  La vista de catálogo **Sys. trace_columns** contiene una lista de todas las columnas de eventos de seguimiento. Estas columnas no cambian para una versión concreta de [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)].  
  
 Para obtener una lista completa de los eventos de seguimiento admitidos, vea [SQL Server referencia](../../relational-databases/event-classes/sql-server-event-class-reference.md)de la clase de eventos.  
  
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)] Use vistas de catálogo de eventos extendidos en su lugar.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**trace_column_id**|**smallint**|Id. único de esta columna.|  
|**name**|**nvarchar(128)**|Nombre único de esta columna. Este parámetro no se traduce.|  
|**type_name**|**nvarchar(128)**|Nombre del tipo de datos de esta columna.|  
|**max_size**|**int**|Tamaño máximo de los datos de esta columna, en bytes.|  
|**is_filterable**|**bit**|Indica si la columna se puede utilizar para especificar un filtro.<br /><br /> 0 = falso<br /><br /> 1 = verdadero|  
|**is_repeatable**|**bit**|Indica si se puede hacer referencia a la columna en los datos de "columna repetida".<br /><br /> 0 = falso<br /><br /> 1 = verdadero|  
|**is_repeated_base**|**bit**|Indica si esta columna se utiliza como clave única para hacer referencia a datos repetidos.<br /><br /> 0 = falso<br /><br /> 1 = verdadero|  
  
## <a name="permissions"></a>Permisos  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Para obtener más información, consulte [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="see-also"></a>Consulte también  
 [Object Catalog Views &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/object-catalog-views-transact-sql.md)  (Vistas de catálogo de objetos [Transact-SQL])  
 [Sys. Traces &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-traces-transact-sql.md)   
 [Sys. trace_categories &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-trace-categories-transact-sql.md)   
 [Sys. trace_events &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-trace-events-transact-sql.md)   
 [Sys. trace_event_bindings &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-trace-event-bindings-transact-sql.md)   
 [Sys. trace_subclass_values &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-trace-subclass-values-transact-sql.md)  
  
  
