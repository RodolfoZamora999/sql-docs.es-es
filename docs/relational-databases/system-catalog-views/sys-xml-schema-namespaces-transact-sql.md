---
description: sys.xml_schema_namespaces (Transact-SQL)
title: sys.xml_schema_namespaces (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.xml_schema_namespaces_TSQL
- sys.xml_schema_namespaces
- xml_schema_namespaces
- xml_schema_namespaces_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.xml_schema_namespaces catalog view
ms.assetid: 3ed42dd6-929a-41de-80e8-d3a0a488bc7a
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 8709142f4ff0e1db417cb67fdb5ea516400ead82
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89545379"
---
# <a name="sysxml_schema_namespaces-transact-sql"></a>sys.xml_schema_namespaces (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Devuelve una fila por espacio de nombres XML definido en XSD. Las tuplas siguientes son únicas: **collection_id**, **namespace_id**, **collection_id**y **Name**.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**xml_collection_id**|**int**|Id. de la colección de esquemas XML que contiene este espacio de nombres.|  
|**name**|**nvarchar(4000)**|Nombre del espacio de nombres XML. **El nombre** en blanco indica que no hay espacio de nombres de destino.|  
|**xml_namespace_id**|**int**|Ordinal en base 1 que identifica de forma exclusiva el espacio de nombres XML en la base de datos.|  
  
## <a name="permissions"></a>Permisos  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Para obtener más información, consulte [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="see-also"></a>Consulte también  
 [Vistas de catálogo &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [Esquemas XML &#40;las vistas de catálogo del sistema de tipos XML&#41; &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/xml-schemas-xml-type-system-catalog-views-transact-sql.md)  
  
  
