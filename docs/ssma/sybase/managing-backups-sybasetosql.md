---
description: Administración de copias de seguridad (SybaseToSQL)
title: Administración de copias de seguridad (SybaseToSQL) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
helpviewer_keywords:
- Tester Component,Managing Backups
ms.assetid: 266d987c-ecc5-4fa4-bfdf-8c584f1a1332
author: nahk-ivanov
ms.author: alexiva
ms.openlocfilehash: 916c0493f477175d9bb92c5fc0db860ea7b375c6
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88372061"
---
# <a name="managing-backups-sybasetosql"></a>Administración de copias de seguridad (SybaseToSQL)
La administración de copia de seguridad de Sybase permite realizar copias de seguridad y restaurar los datos de las tablas antes o después de ejecutar una prueba. También puede administrar el cuadro de diálogo contenido de copia de seguridad con administrar contenido de copia de seguridad.  
  
## <a name="sybase-backup-management"></a>Administración de copia de seguridad de Sybase  
  
### <a name="backup"></a>Copia de seguridad  
Para abrir el cuadro de diálogo copia de seguridad, en el menú evaluador, seleccione Sybase backup Management y, a continuación, haga clic en copia de seguridad.... En el cuadro de diálogo copia de seguridad encontrará el árbol de metadatos de Sybase en el que se muestran todas las tablas del esquema de Sybase cargado. Seleccione una o más tablas para realizar una copia de seguridad.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **copia** de seguridad para hacer una copia de seguridad de los datos de la tabla.  
  
-   Haga clic en el botón **Cancelar** para cerrar el cuadro de diálogo.  
  
### <a name="restore"></a>Restauración  
Para abrir el cuadro de diálogo restaurar, en el menú evaluador, seleccione Sybase backup Management y, a continuación, haga clic en restaurar.... Allí encontrará un árbol que contiene las tablas disponibles en la copia de seguridad. Seleccione una o más tablas para restaurar sus datos.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **restaurar** para restaurar los datos de copia de seguridad en la tabla.  
  
-   Haga clic en el botón **Cancelar** para cerrar el cuadro de diálogo.  
  
### <a name="managing-backup-contents"></a>Administrar contenido de copia de seguridad  
Para abrir administrar contenido de copia de seguridad, en el menú evaluador, seleccione Sybase backup Management y, a continuación, haga clic en copia de seguridad de contenido.... Allí encontrará un árbol que contiene las tablas de la copia de seguridad.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **quitar** para quitar la tabla de la copia de seguridad.  
  
-   Haga clic en el botón **cerrar** para cerrar el cuadro de diálogo.  
  
## <a name="sql-server-backup-management"></a>Administración de copia de seguridad de SQL Server  
SQL Server administración de copias de seguridad permite realizar copias de seguridad y restaurar los datos de las tablas antes o después de ejecutar una prueba. También puede administrar el cuadro de diálogo contenido de copia de seguridad con administrar contenido de copia de seguridad.  
  
### <a name="backup"></a>Copia de seguridad  
Para abrir el cuadro de diálogo copia de seguridad, en el menú evaluador, seleccione SQL Server administración de copia de seguridad y haga clic en copia de seguridad..... En el cuadro de diálogo copia de seguridad, encontrará el SQL Server árbol de metadatos que muestra todas las tablas de las bases de datos SQL Server cargadas. Seleccione una o más tablas para realizar una copia de seguridad.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **copia** de seguridad para hacer una copia de seguridad de los datos de la tabla.  
  
-   Haga clic en el botón **Cancelar** para cerrar el cuadro de diálogo.  
  
### <a name="restore"></a>Restauración  
Para abrir el cuadro de diálogo restaurar, en el menú comprobador, seleccione SQL Server administración de copia de seguridad, haga clic en restaurar.... Allí encontrará un árbol que contiene las tablas disponibles en la copia de seguridad. Seleccione una o más tablas para restaurar sus datos.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **restaurar** para restaurar los datos de copia de seguridad en la tabla.  
  
-   Haga clic en el botón **Cancelar** para cerrar el cuadro de diálogo.  
  
### <a name="managing-backup-contents"></a>Administrar contenido de copia de seguridad  
Para abrir administrar contenido de copia de seguridad, en el menú comprobador, seleccione SQL Server administración de copia de seguridad y haga clic en copia de seguridad de contenido.... Allí encontrará un árbol que contiene las tablas de la copia de seguridad.  
  
En el cuadro de diálogo están disponibles los siguientes botones:  
  
-   Haga clic en el botón **comprobar estado** para comprobar el estado de copia de seguridad de la tabla.  
  
-   Haga clic en el botón **quitar** para quitar la tabla de la copia de seguridad.  
  
-   Haga clic en el botón **cerrar** para cerrar el cuadro de diálogo.  
  
## <a name="see-also"></a>Consulte también  
[Probar objetos de base de datos migrados &#40;SybaseToSQL&#41;](../../ssma/sybase/testing-migrated-database-objects-sybasetosql.md)  
  
