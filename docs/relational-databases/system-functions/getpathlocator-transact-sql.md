---
description: GetPathLocator (Transact-SQL)
title: Función getpathlocator (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- GetPathLocator
- GetPathLocator_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- GetPathLocator function
ms.assetid: 78b7e220-445b-4fdf-811b-7253f4f2b058
author: rothja
ms.author: jroth
ms.openlocfilehash: 2551dfbb7d71b33542f4bc6fd8087c10f974e45b
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88464769"
---
# <a name="getpathlocator-transact-sql"></a>GetPathLocator (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Devuelve el valor del identificador del localizador de ruta de acceso para el archivo o directorio especificado en un objeto FileTable.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
GetPathLocator(filenamespace_path)  
```  
  
## <a name="arguments"></a>Argumentos  
 *filenamespace_path*  
 Ruta de acceso del espacio de nombres en el objeto FileTable. La ruta de acceso del espacio de nombres es de tipo **nvarchar (Max)**.  
  
 Cuando la base de datos pertenece a un grupo de disponibilidad de Always On, la función **función getpathlocator** acepta el nombre de red virtual (VNN) o el nombre de equipo.  
  
## <a name="return-type"></a>Tipo de valor devuelto  
 **hierarchyid**  
  
## <a name="general-remarks"></a>Notas generales  
 Para más información, consulte [Work with Directories and Paths in FileTables](../../relational-databases/blob/work-with-directories-and-paths-in-filetables.md).  
  
## <a name="examples"></a>Ejemplos  
 Puede usar la función **función getpathlocator** al migrar archivos de un servidor de archivos a una filetable. En este escenario, puede mover los archivos al objeto FileTable y reemplazar después la ruta de acceso UNC original para cada archivo por la ruta de acceso UNC del objeto FileTable. Para obtener un ejemplo completo, consulte [carga de archivos en FileTables](../../relational-databases/blob/load-files-into-filetables.md).  
  
## <a name="see-also"></a>Consulte también  
 [Trabajar con directorios y rutas de acceso de FileTables](../../relational-databases/blob/work-with-directories-and-paths-in-filetables.md)  
  
  
