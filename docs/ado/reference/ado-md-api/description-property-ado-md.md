---
description: Description (propiedad) (ADO MD)
title: Propiedad Description (ADO MD) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Member::Description
- Level::Description
- CubeDef::Description
- Hierarchy::Description
- Description
- Dimension::Description
helpviewer_keywords:
- Description property [ADO MD]
ms.assetid: 6d626d35-0bf3-4f24-9934-ad9c9c91273a
author: rothja
ms.author: jroth
ms.openlocfilehash: 726a49da64c36b487868068affad65164b9b3c5e
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88986906"
---
# <a name="description-property-ado-md"></a>Description (propiedad) (ADO MD)
Devuelve una explicación de texto del objeto actual.  
  
## <a name="return-values"></a>Valores devueltos  
 Devuelve una **cadena** y es de solo lectura.  
  
## <a name="remarks"></a>Observaciones  
 En el caso de los objetos [miembro](./member-object-ado-md.md) , la **Descripción** solo se aplica a los miembros Measure y formula. **Description** devuelve una cadena vacía ("") para todos los demás tipos de miembros. Para obtener más información sobre los distintos tipos de miembros, vea la propiedad [Type](./type-property-ado-md.md) .  
  
 Esta propiedad solo se admite en los objetos **member** que pertenezcan a un objeto [LEVEL](./level-object-ado-md.md) . Se produce un error cuando se hace referencia a esta propiedad desde objetos **member** que pertenecen a un objeto [Position](./position-object-ado-md.md) .  
  
## <a name="applies-to"></a>Se aplica a  

:::row:::
    :::column:::
        [Objeto CubeDef (ADO MD)](./cubedef-object-ado-md.md)  
        [Objeto de dimensión (ADO MD)](./dimension-object-ado-md.md)  
    :::column-end:::
    :::column:::
        [Objeto Hierarchy (ADO MD)](./hierarchy-object-ado-md.md)  
        [Objeto Level (ADO MD)](./level-object-ado-md.md)  
    :::column-end:::
    :::column:::
        [Objeto de miembro (ADO MD)](./member-object-ado-md.md)  
    :::column-end:::
:::row-end:::