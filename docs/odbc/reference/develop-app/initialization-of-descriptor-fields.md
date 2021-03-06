---
description: Inicialización de campos de Descriptor
title: Inicialización de campos de descriptor | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- descriptors [ODBC], allocating and freeing
- initializing descriptor fields [ODBC]
- allocating and freeing descriptors [ODBC]
ms.assetid: 1da157cb-8ea9-4a56-983b-1c45650217c5
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 2537e5e74c600c72368e46bda7640b881d9a34df
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88424657"
---
# <a name="initialization-of-descriptor-fields"></a>Inicialización de campos de Descriptor
Cuando se asigna un descriptor de fila de aplicación, sus campos reciben los valores iniciales que se indican en [SQLSetDescField](../../../odbc/reference/syntax/sqlsetdescfield-function.md). El valor inicial del campo SQL_DESC_TYPE es SQL_DEFAULT. Esto proporciona un tratamiento estándar de los datos de la base de datos para su presentación en la aplicación. La aplicación puede especificar un tratamiento diferente de los datos estableciendo los campos del registro del descriptor.  
  
 El valor inicial de SQL_DESC_ARRAY_SIZE en el encabezado del descriptor es 1. La aplicación puede modificar este campo para habilitar la recuperación de varias filas.  
  
 El concepto de un valor predeterminado no es válido para los campos de un IRD. Una aplicación puede obtener acceso a los campos de un IRD solo cuando hay una instrucción preparada o ejecutada asociada.  
  
 Ciertos campos de un IPD se definen solo después de que el controlador haya rellenado automáticamente IPD. Si no es así, son indefinidos. Estos campos son SQL_DESC_CASE_SENSITIVE, SQL_DESC_FIXED_PREC_SCALE, SQL_DESC_TYPE_NAME, SQL_DESC_UNSIGNED y SQL_DESC_LOCAL_TYPE_NAME.
