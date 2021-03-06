---
description: sys.dm_broker_forwarded_messages (Transact-SQL)
title: Sys. dm_broker_forwarded_messages (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.dm_broker_forwarded_messages
- dm_broker_forwarded_messages
- sys.dm_broker_forwarded_messages_TSQL
- dm_broker_forwarded_messages_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_broker_forwarded_messages dynamic management view
ms.assetid: 5576376d-6364-417a-8475-aa770e060845
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 1b167baced0acda08234b4240bc362c602f327f9
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89544797"
---
# <a name="sysdm_broker_forwarded_messages-transact-sql"></a>sys.dm_broker_forwarded_messages (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Devuelve una fila por cada mensaje de Service Broker que una instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] tiene en proceso de reenvío.  
  

|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**conversation_id**|**uniqueidentifier**|Id. de la conversación a la que pertenece este mensaje. Acepta valores NULL.|  
|**is_initiator**|**bit**|Indica si este mensaje es del iniciador de la conversación.  Acepta valores NULL.<br /><br /> 0 = No es del iniciador.<br /><br /> 1 = Es del iniciador|  
|**to_service_name**|**nvarchar(512)**|Nombre del servicio al que se envía este mensaje. Acepta valores NULL.|  
|**to_broker_instance**|**nvarchar(512)**|Identificador del agente que hospeda el servicio al que se envía este mensaje. Acepta valores NULL.|  
|**from_service_name**|**nvarchar(512)**|Nombre del servicio que origina este mensaje. Acepta valores NULL.|  
|**from_broker_instance**|**nvarchar(512)**|Identificador del agente que hospeda el servicio de donde viene este mensaje. Acepta valores NULL.|  
|**adjacent_broker_address**|**nvarchar(512)**|Dirección de red a la que se envía este mensaje. Acepta valores NULL.|  
|**message_sequence_number**|**bigint**|Número de secuencia del mensaje en el cuadro de diálogo. Acepta valores NULL.|  
|**message_fragment_number**|**int**|Si el mensaje de diálogo está fragmentado, es el número de fragmento que contiene este mensaje de transporte. Acepta valores NULL.|  
|**hops_remaining**|**tinyint**|Número de veces que se puede retransmitir el mensaje antes de que llegue el destino final. Cada vez que se reenvía el mensaje, este número disminuye en 1. Acepta valores NULL.|  
|**time_to_live**|**int**|Tiempo máximo en que el mensaje permanece activo. Cuando llega a 0, el mensaje se descarta. Acepta valores NULL.|  
|**time_consumed**|**int**|Tiempo que el mensaje ha estado activo. Cada vez que se reenvía el mensaje, este número aumenta en el tiempo que ha tardado en reenviarse el mensaje. No acepta valores NULL.|  
|**message_id**|**uniqueidentifier**|Id. del mensaje. Acepta valores NULL.|  
  
## <a name="permissions"></a>Permisos  
 es necesario contar con el permiso VIEW SERVER STATE en el servidor.  
  
## <a name="see-also"></a>Consulte también  
 [Funciones y vistas de administración dinámica &#40;Transact-SQL&#41;](~/relational-databases/system-dynamic-management-views/system-dynamic-management-views.md)   
 [Vistas de administración dinámica relacionadas con Service Broker &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/service-broker-related-dynamic-management-views-transact-sql.md)  
  
  

