---
title: Apertura, consulta e impresión de un archivo de interbloqueo (SSMS)
description: Obtenga más información sobre cómo capturar información de interbloqueo que genera SQL Server Profiler y cómo verla en SQL Server Management Studio.
ms.custom: seo-dt-2019
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: performance
ms.topic: conceptual
helpviewer_keywords:
- deadlocks [SQL Server], printing files
- deadlocks [SQL Server], opening files
- opening deadlock files
- printing deadlock files
ms.assetid: 5061b13f-2cb7-457a-b8d0-fbd437b510ab
author: julieMSFT
ms.author: jrasnick
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: 3c55ad170e9d6a9fe58865ab28ac75f018b6905b
ms.sourcegitcommit: 9470c4d1fc8d2d9d08525c4f811282999d765e6e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "86458514"
---
# <a name="open-view-and-print-a-deadlock-file-in-sql-server-management-studio-ssms"></a>Apertura, consulta e impresión de un archivo de interbloqueo en SQL Server Management Studio (SSMS)

[!INCLUDE [SQL Server Azure SQL Database](../../includes/applies-to-version/sql-asdb.md)]
  Cuando [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] genera un interbloqueo, puede capturar y guardar la información de interbloqueo en un archivo. Después de guardar el archivo de interbloqueo, puede abrirlo en [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] para verlo o imprimirlo.  
  
## <a name="open-and-view-a-deadlock-file"></a>Abrir y ver un archivo de interbloqueo  
  
1. En el menú **Archivo** de [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], seleccione **Abrir** y, a continuación, **Archivo**.  
  
2. En el cuadro de diálogo **Abrir archivo** , en **Archivos de tipo** , seleccione el tipo de archivo .xdl. Se mostrará una lista filtrada en la que solo aparecerán archivos de interbloqueo.  
  
## <a name="print-a-deadlock-file"></a>Imprimir un archivo de interbloqueo  
  
1. En el menú **Archivo** de [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], seleccione **Abrir** y, a continuación, **Archivo**.  
  
2. En el cuadro de diálogo **Abrir archivo** , en **Archivos de tipo** , seleccione el tipo de archivo .xdl. Se mostrará una lista filtrada en la que solo aparecerán archivos de interbloqueo.  
  
3. Seleccione el archivo de interbloqueo que quiera imprimir y, a continuación, **Abrir**.  
  
4. En el menú **Archivo**, seleccione **Imprimir**.  
  
## <a name="see-also"></a>Consulte también  
 [Guardar grafos de interbloqueo &#40;SQL Server Profiler&#41;](../../relational-databases/performance/save-deadlock-graphs-sql-server-profiler.md)  
  
  
