---
description: Estados de validación (Master Data Services)
title: Estados de validación
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: mds
ms.reviewer: ''
ms.technology: master-data-services
ms.topic: conceptual
ms.assetid: fc829d25-b3e8-4801-8a94-4df19a7a5971
author: lrtoyou1223
ms.author: lle
ms.openlocfilehash: 7d0dd3f4589f18cd7eb94fab61937a7452a94f35
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88491535"
---
# <a name="validation-statuses-master-data-services"></a>Estados de validación (Master Data Services)

[!INCLUDE [SQL Server - Windows only ASDBMI  ](../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  En el área funcional **Administración de versiones** , en la página **Validar versión** , se pueden dar los siguientes estados.  
  
|Estado|Descripción|  
|------------|-----------------|  
|Esperando la validación|Todos los miembros que se acaben de crear que esperen ser validados.|  
|Esperando la revalidación|Miembros existentes que estén esperando ser validados.|  
|Validación correcta|Miembros que pasaron la validación de las reglas de negocios.|  
|Error de validación|Miembros con error de validación en las reglas de negocios.|  
|Esperando la revalidación de los miembros dependientes|Miembros consolidados actualizados que esperen ser validados junto con los miembros secundarios.|  
  
## <a name="see-also"></a>Consulte también  
 [Validar una versión con las reglas de negocios &#40;Master Data Services&#41;](../master-data-services/validate-a-version-against-business-rules-master-data-services.md)   
 [Versiones &#40;Master Data Services&#41;](../master-data-services/versions-master-data-services.md)  
  
  
