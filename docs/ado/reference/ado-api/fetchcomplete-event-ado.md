---
description: Evento FetchComplete (ADO)
title: Evento FetchComplete (ADO) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Recordset::ExecuteComplete
- ExecuteComplete
helpviewer_keywords:
- FetchComplete event [ADO]
ms.assetid: a28d3858-566c-468d-b070-d1de4339fbea
author: rothja
ms.author: jroth
ms.openlocfilehash: 7ef8df9f6d4ea113d5cca9ad9ffba9c4888776d8
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88973356"
---
# <a name="fetchcomplete-event-ado"></a>Evento FetchComplete (ADO)
Se llama al evento **FetchComplete** después de que todos los registros de una operación asincrónica larga se hayan recuperado en el [conjunto de registros](../../../ado/reference/ado-api/recordset-object-ado.md).  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
FetchComplete pError, adStatus, pRecordset  
```  
  
#### <a name="parameters"></a>Parámetros  
 *pError*  
 Un objeto de [error](../../../ado/reference/ado-api/error-object.md) . Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece.  
  
 *adStatus*  
 Valor de estado de [EventStatusEnum](../../../ado/reference/ado-api/eventstatusenum.md) . Cuando se llama a este evento, este parámetro se establece en **adStatusOK** si la operación que causó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.  
  
 Antes de que se devuelva este evento, establezca este parámetro en **adStatusUnwantedEvent** para evitar notificaciones posteriores.  
  
 *pRecordset*  
 Objeto de **conjunto de registros** . Objeto para el que se recuperaron los registros.  
  
## <a name="remarks"></a>Observaciones  
 Para usar **FetchComplete** con Microsoft Visual Basic, se requiere Visual Basic 6,0 o posterior.  
  
## <a name="see-also"></a>Consulte también  
 [Ejemplo de modelo de eventos de ADO (VC + +)](../../../ado/reference/ado-api/ado-events-model-example-vc.md)   
 [Conexión ADO y los eventos de conjunto de registros](../../../ado/guide/data/ado-event-handler-summary.md)
