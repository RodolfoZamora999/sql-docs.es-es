---
description: Sys. dm_cluster_endpoints (Transact-SQL)
title: Sys. dm_cluster_endpoints (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2019
ms.prod: sql
ms.prod_service: database-engine, big-data-clusters
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.dm_cluster_endpoints
- dm_cluster_endpoints_TSQL
- dm_cluster_endpoints
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_cluster_endpoints dynamic management view
ms.assetid: ''
author: markingmyname
ms.author: maghan
monikerRange: '>=sql-server-ver15||=sqlallproducts-allversions||>=sql-server-linux-2017'
ms.openlocfilehash: 7df88a6be24e5378a8bd588514c9806e8258eb0e
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89542348"
---
# <a name="sysdm_cluster_endpoints-transact-sql"></a>Sys. dm_cluster_endpoints (Transact-SQL)
[!INCLUDE[sqlserver2019](../../includes/applies-to-version/sqlserver2019.md)]

|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|name|`sysname`|Nombre del servicio expuesto externamente en un clúster de macrodatos de SQL. Identificador único para el extremo. Clave para esta vista. No admite valores NULL. |  
|description|`nvarchar(4000)`|Descripción del servicio. No admite valores NULL. |
|endpoint|`sysname`|Dirección URL del extremo o atributo de conexión. No admite valores NULL. |
|protocol_desc|`sysname`|Descripción del Protocolo de extremo |

## <a name="permissions"></a>Permisos

En [!INCLUDE[ssNoVersion_md](../../includes/ssnoversion-md.md)] , requiere el `VIEW SERVER STATE` permiso.

## <a name="see-also"></a>Consulte también

[¿Qué [!INCLUDE[big-data-clusters-2019](../../includes/ssbigdataclusters-ss-nover.md)] son ](../../big-data-cluster/big-data-cluster-overview.md)?
