---
title: Evaluación de una directiva de administración basada en directivas desde un objeto
description: Obtenga información sobre cómo evaluar una directiva a partir de una instancia de SQL Server, una base de datos o un objeto de base de datos mediante SQL Server Management Studio (SSMS).
ms.custom: seo-lt-2019
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: security
ms.topic: conceptual
helpviewer_keywords:
- Policy-Based Management, evaluate policy
ms.assetid: b9e9d646-4894-4dee-a02a-0c71a8dc020e
author: VanMSFT
ms.author: vanto
ms.openlocfilehash: 66171e02a8a33ff96d6de6ecb3e4a2c990c9affb
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "85654253"
---
# <a name="evaluate-a-policy-based-management-policy-from-an-object"></a>Evaluar una directiva de administración basada en directivas desde un objeto
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  En este tema se describe cómo evaluar una directiva de una instancia de servidor, una base de datos o un objeto de base de datos en [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] mediante [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)].  
  
 **En este tema**  
  
-   **Antes de empezar:**  
  
     [Limitaciones y restricciones](#Restrictions)  
  
     [Seguridad](#Security)  
  
-   **Para evaluar una directiva de un objeto mediante:**  
  
     [SQL Server Management Studio](#SSMSProcedure)  
  
##  <a name="before-you-begin"></a><a name="BeforeYouBegin"></a> Antes de comenzar  
  
###  <a name="limitations-and-restrictions"></a><a name="Restrictions"></a> Limitaciones y restricciones  
  
-   El modo de ejecución se define como parte de la directiva y no se puede cambiar en el cuadro de diálogo **Evaluar directivas** .  
  
-   El cuadro de diálogo **Evaluar directivas** solo muestra las directivas apropiadas para el objeto de base de datos.  
  
###  <a name="security"></a><a name="Security"></a> Seguridad  
  
####  <a name="permissions"></a><a name="Permissions"></a> Permisos  
 Requiere la pertenencia al rol PolicyAdministratorRole en la base de datos msdb.  
  
##  <a name="using-sql-server-management-studio"></a><a name="SSMSProcedure"></a> Uso de SQL Server Management Studio  
  
#### <a name="to-evaluate-a-policy-from-an-object"></a>Para evaluar una directiva de un objeto  
  
1.  En el Explorador de objetos, haga clic con el botón derecho en una instancia de servidor, base de datos u objeto de base de datos, elija **Directivas**y, después, seleccione **Evaluar**.  
  
2.  En el cuadro de diálogo **Evaluar directivas** , seleccione una o varias directivas y haga clic en **Evaluar** para ejecutar la directiva en modo de evaluación. De esta forma se genera un informe de compatibilidad para el conjunto de destino, pero no se vuelve a configurar [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ni se exige la compatibilidad en el futuro. En los destinos que no obedecen las directivas seleccionadas y que tienen propiedades que pueden estar reconfiguradas por la administración basada en directivas, puede exigir la compatibilidad de la directiva haciendo clic en **Aplicar**. Para obtener más información acerca de las opciones disponibles en el cuadro de diálogo **Evaluar directivas** , vea [Evaluate Policies Dialog Box, Policy Selection Page](../../relational-databases/policy-based-management/evaluate-policies-dialog-box-policy-selection-page.md), [Evaluate Policies Dialog Box, Evaluation Results Page](../../relational-databases/policy-based-management/evaluate-policies-dialog-box-evaluation-results-page.md)y [Results Detailed View Dialog Box](../../relational-databases/policy-based-management/results-detailed-view-dialog-box.md).  
  
3.  Cuando termine, haga clic en **Cerrar**.  
  
  
