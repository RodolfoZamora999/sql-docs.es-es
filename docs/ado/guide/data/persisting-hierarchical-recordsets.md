---
description: Almacenar conjuntos de registros jerárquicos
title: Conservar conjuntos de registros jerárquicos | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- hierarchical Recordsets [ADO], persisting
- persisting hierarchical Recordsets [ADO]
- data shaping [ADO], hierarchical Recordsets
ms.assetid: 43798bb5-98a6-4ad6-9bf8-78154b3a1827
author: rothja
ms.author: jroth
ms.openlocfilehash: b3764011c0ce0e3a49a17b20cbb344b5e98218d7
ms.sourcegitcommit: c7f40918dc3ecdb0ed2ef5c237a3996cb4cd268d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "91724956"
---
# <a name="persisting-hierarchical-recordsets"></a>Almacenar conjuntos de registros jerárquicos
Puede guardar un **conjunto de registros** jerárquico en un archivo en formato ADTG o XML llamando al método [Save](../../../ado/reference/ado-api/save-method.md) . Sin embargo, se aplican dos limitaciones al guardar los **conjuntos de registros**jerárquicos en formato XML: no se puede guardar en XML si el **conjunto de registros** jerárquico contiene actualizaciones pendientes y no se puede guardar un conjunto de **registros**jerárquico con parámetros.  
  
 Para obtener más información sobre el proveedor de forma de datos, vea servicio de forma [de datos de Microsoft para OLE DB](../../../ado/guide/appendixes/microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) e [información general sobre el servicio de forma de datos para OLE DB](/previous-versions/windows/desktop/ms719615(v=vs.85)).  
  
## <a name="see-also"></a>Consulte también  
 [Ejemplo de forma de datos](../../../ado/guide/data/data-shaping-example.md)   
 [Gramática de forma formal](../../../ado/guide/data/formal-shape-grammar.md)   
 [Comandos Shape en General](../../../ado/guide/data/shape-commands-in-general.md)