---
description: MSSQLSERVER_10538
title: MSSQLSERVER_10538 | Microsoft Docs
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: language-reference
helpviewer_keywords:
- 10538 (Database Engine error)
ms.assetid: 284d19b4-4979-4cbe-a9be-ac1104433c69
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: b938580c448f0073784e58763d35f4a795317c44
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88338201"
---
# <a name="mssqlserver_10538"></a>MSSQLSERVER_10538
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Detalles  
  
| Atributo | Value |  
| :-------- | :---- |  
|Nombre de producto|SQL Server|  
|Id. de evento|10538|  
|Origen de eventos|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|PG_INVALID_PLANGUIDE_HANDLE|  
|Texto del mensaje|No se encuentra la guía de plan porque el Id. de guía de plan especificado es NULL o no es válido, o porque no tiene permiso para el objeto al que hace referencia la guía de plan. Compruebe que el id. de guía de plan es válido, la sesión actual está establecida en el contexto de base de datos correcto y que tiene permiso ALTER para el objeto al que hace referencia la guía de plan o el permiso ALTER DATABASE.|  
  
## <a name="explanation"></a>Explicación  
El identificador de la guía de plan especificada es NULL o no es válido, o no se tiene permiso para el objeto al que hace referencia la guía de plan.  
  
## <a name="user-action"></a>Acción del usuario  
Compruebe que el identificador de guía de plan es válido, la sesión actual está establecida en el contexto de base de datos correcto y se tiene el permiso ALTER DATABASE o ALTER para el objeto al que hace referencia la guía de plan.  
  
## <a name="see-also"></a>Consulte también  
[sp_create_plan_guide &#40;Transact-SQL&#41;](~/relational-databases/system-stored-procedures/sp-create-plan-guide-transact-sql.md)  
[Guías de plan](~/relational-databases/performance/plan-guides.md)  
[sp_create_plan_guide_from_handle &#40;Transact-SQL&#41;](~/relational-databases/system-stored-procedures/sp-create-plan-guide-from-handle-transact-sql.md)  
  
