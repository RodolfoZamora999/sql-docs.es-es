---
description: StreamOpenOptionsEnum
title: StreamOpenOptionsEnum | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- StreamOpenOptionsEnum
helpviewer_keywords:
- StreamOpenOptionsEnum enumeration [ADO]
ms.assetid: 85b6c57f-47ed-46ba-bd92-07882ae9e9d2
author: rothja
ms.author: jroth
ms.openlocfilehash: 8f3865a3b0e550e7e3fe4887fb948bca72eadf1b
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88988506"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum
Especifica las opciones para abrir un objeto de [flujo](./stream-object-ado.md) . Los valores se pueden combinar con una operación o.  
  
|Constante|Valor|Descripción|  
|--------------|-----------|-----------------|  
|**adOpenStreamAsync**|1|Abre el objeto de **secuencia** en modo asincrónico.|  
|**adOpenStreamFromRecord**|4|Identifica el contenido del parámetro de *origen* para que sea un objeto de [registro](./record-object-ado.md) ya abierto. El comportamiento predeterminado es tratar el *origen* como una dirección URL que apunta directamente a un nodo en una estructura de árbol. Se abre el flujo predeterminado asociado a ese nodo.|  
|**adOpenStreamUnspecified**|-1|Predeterminada. Especifica la apertura del objeto de **secuencia** con opciones predeterminadas.|  
  
## <a name="adowfc-equivalent"></a>Equivalente de ADO/WFC  
 Estas constantes no tienen equivalentes de ADO/WFC.  
  
## <a name="applies-to"></a>Se aplica a  
 [Open (método) (Stream de ADO)](./open-method-ado-stream.md)