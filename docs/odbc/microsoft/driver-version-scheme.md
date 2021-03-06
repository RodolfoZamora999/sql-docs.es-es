---
description: Esquema de la versión de controlador
title: Esquema de versión del controlador | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- ODBC driver for Oracle [ODBC], versions
ms.assetid: e4a8d9d7-8aba-48ab-8be6-1a6129adfb8f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0414da00ffc5a220e3bf6b13837880b1116f58eb
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88412731"
---
# <a name="driver-version-scheme"></a>Esquema de la versión de controlador
> [!IMPORTANT]  
>  Esta característica se quitará en una versión futura de Windows. Evite utilizar esta característica en nuevos trabajos de desarrollo y tenga previsto modificar las aplicaciones que actualmente la utilizan. En su lugar, utilice el controlador ODBC proporcionado por Oracle.  
  
 En la tabla siguiente se enumeran todas las versiones publicadas de Microsoft ODBC driver for Oracle.  
  
|Versión del controlador|Número de compilación|Historial de disponibilidad|  
|--------------------|------------------|--------------------------|  
|1.0|2.00.6235|Visual C++ 4,2 y Visual Basic 5,0, Enterprise Edition|  
|2.0|2.73.7269|Visual Studio 97 y MDAC 1.5 a|  
|2,0 actualizado|2.73.7283.01|IIS 4,0|  
|2,0 actualizado|2.73.7283.03|MDAC 1.5 b y 1.5 c|  
|2,0 actualizado|2.73.7356|SDK DE ODBC 3,5|  
|2.5|2.573.2927|Visual Studio 6,0 y MDAC 2,0|  
|2,5 actualizado|2.573.3513|SQL Server 7,0<br /><br /> SQL Server 6,5 SP5|  
  
 Build 2.00.6235 (versión 1) fue la primera versión de Microsoft ODBC driver for Oracle. Después del lanzamiento de la primera versión, se adoptó una nueva Convención de nomenclatura.  
  
 Por ejemplo, 2.73.7283.03 se puede dividir en los siguientes componentes distintos:  
  
-   2 = el número de versión.  
  
-   73 = versión del servidor de Oracle para el que se diseñó el controlador.  
  
-   7283,03 = el número de compilación del controlador.  
  
> [!NOTE]  
>  Con la versión 2.573.2973, la Convención de nomenclatura ha provocado una confusión que 2,573 es una versión anterior a 2,73, pero cada sección del número de compilación se debe considerar individualmente. El número 573 es mayor que 73, por lo que es una versión más reciente. Además, "2,5" indica el número de versión del controlador.
