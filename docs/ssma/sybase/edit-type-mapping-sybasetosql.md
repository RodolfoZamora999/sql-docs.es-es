---
description: Editar asignación de tipo (SybaseToSQL)
title: Editar la asignación de tipos (SybaseToSQL) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
ms.assetid: 513f071a-d5e6-4ed5-acca-269bf76323c5
author: nahk-ivanov
ms.author: alexiva
ms.openlocfilehash: 3f9f5e0f498dbe6a8fe45a9c80cbf3c512f04bac
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88492289"
---
# <a name="edit-type-mapping-sybasetosql"></a>Editar asignación de tipo (SybaseToSQL)
El cuadro de diálogo **Editar asignación de tipos** permite especificar cómo se asignan los tipos entre los objetos de base de datos de origen y de destino.  
  
Puede tener acceso a este cuadro de diálogo en varios lugares:  
  
-   Al seleccionar una base de datos de origen o un objeto de base de datos, la pestaña **asignación de tipos** aparece a la derecha del explorador de metadatos. Haga clic en **Agregar** para agregar una nueva asignación de tipos o haga clic en **Editar** para cambiar una asignación de tipos existente.  
  
-   En el menú **herramientas** , seleccione **configuración del proyecto** o **configuración predeterminada del proyecto**. En el cuadro de diálogo resultante, seleccione **asignación de tipos**. Haga clic en **Agregar** para agregar una nueva asignación de tipos o haga clic en **Editar** para cambiar una asignación de tipos existente.  
  
Las asignaciones de tipos específicas de tabla invalidan las asignaciones de tipo de proyecto y base de datos. Las asignaciones específicas de la base de datos invalidan las asignaciones del proyecto.  
  
## <a name="options"></a>Opciones  
**Tipo de origen**  
Seleccione el tipo de datos de origen que se va a asignar a un [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] tipo de datos.  
  
Si el tipo de datos es de longitud variable, los campos siguientes aparecerán en **tipo de origen**:  
  
**From**  
Especifique la longitud mínima de esta asignación. Por ejemplo, para el tipo de datos **nchar** , puede especificar 10 para especificar que esta asignación es para un intervalo que empieza en **NCHAR (10)**.  
  
**To**  
Especifique la longitud máxima de esta asignación. Por ejemplo, para el tipo de datos **nchar** , puede especificar 20 para especificar que esta asignación es para un intervalo que termina en **NCHAR (20)**.  
  
**Tipo de destino**  
Seleccione el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] tipo de datos al que se asigna el tipo de datos de origen. Cuando SSMA crea la tabla o el procedimiento almacenado en [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] , el tipo de datos de origen cambiará a este tipo de datos.  
  
Si el tipo de datos es de longitud variable, el siguiente campo aparecerá en **tipo de destino**:  
  
**Replace with**  
Especifique la longitud de destino de esta asignación. Por ejemplo, para el tipo de datos **nvarchar** , puede especificar 20 para especificar que el tipo de datos de origen especificado debe estar asignado a **nvarchar (20)**.  
  
