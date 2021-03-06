---
title: SQL Server XTP IO Governor | Microsoft Docs
description: Obtenga información sobre el objeto de rendimiento SQL Server XTP IO Governor, que contiene contadores relacionados con el regulador de tasa de E/S de OLPT en memoria.
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: performance
ms.topic: conceptual
ms.assetid: 91e176fe-c838-44e9-b4fc-2814a0551ca3
author: julieMSFT
ms.author: jrasnick
ms.openlocfilehash: ca71e9d90cf5e057d70a32eae9882d90ddbcf611
ms.sourcegitcommit: 9470c4d1fc8d2d9d08525c4f811282999d765e6e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "86457947"
---
# <a name="sql-server-xtp-io-governor"></a>SQL Server XTP IO Governor
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

El objeto de rendimiento SQL Server XTP IO Governor contiene contadores relacionados con el regulador de frecuencia de E/S OLPT en memoria.

En esta tabla se describen los contadores de **SQL Server XTP IO Governor** .

|Contador|Descripción|  
|-------------|-----------------|  
|**Esperas de créditos por segundo insuficientes**|Número de esperas debido a créditos insuficientes en los objetos de frecuencia (por segundo).|
|**E/S emitidas por segundo**|Número de E/S emitidas por segundo por los subprocesos de vaciado.|
|**Bloqueos de registro por segundo**|Número de bloqueos de registro procesados por el controlador por segundo.|
|**Ranuras de crédito perdidas**|Número de ranuras de crédito perdidas debido a la espera de créditos de objeto de frecuencia.|
|**Esperas por segundo de objetos de frecuencia obsoletos**|Número de esperas debido a objetos de frecuencia obsoletos (por segundo).|
|**Objetos de frecuencia totales publicados**|Número total de objetos de frecuencia publicados.|
 

## <a name="see-also"></a>Consulte también  
[Contadores de rendimiento de XTP &#40;OLTP en memoria&#41;](../../relational-databases/performance-monitor/sql-server-xtp-in-memory-oltp-performance-counters.md)
