---
description: Notas de implementación
title: Notas de implementación | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: 7ec14b9c-69b8-4c6e-838a-88d1ebdc8725
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7117e0d8af856a16a47414f5a8c3ec11c475cb92
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88483268"
---
# <a name="implementation-notes"></a>Notas de implementación
> [!IMPORTANT]  
>  Esta característica se quitará en una versión futura de Windows. Evite usar esta característica en los nuevos trabajos de desarrollo y planee modificar las aplicaciones que actualmente la utilizan. Microsoft recomienda el uso de la funcionalidad de cursor del controlador.  
  
 En esta sección se describe cómo se implementa la biblioteca de cursores ODBC. Describe cómo la biblioteca de cursores mantiene su memoria caché, ejecuta instrucciones SQL e implementa funciones ODBC.  
  
 Esta sección contiene los temas siguientes.  
  
-   [Caché de la biblioteca de cursores](../../../odbc/reference/appendixes/cursor-library-cache.md)  
  
-   [Procesamiento de instrucciones SQL](../../../odbc/reference/appendixes/processing-sql-statements.md)  
  
-   [Funciones ODBC y biblioteca de cursores](../../../odbc/reference/appendixes/odbc-functions-and-the-cursor-library.md)
