---
title: Números de error nativos | Microsoft Docs
description: En el caso de los errores, el controlador ODBC de SQL Server Native Client devuelve el número de error nativo de SQL Server o, en el caso de los errores detectados por el controlador, 0.
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
helpviewer_keywords:
- ODBC error handling, native error numbers
- SQL Server Native Client ODBC driver, errors
- native error numbers [SQL Server Native Client]
- messages [ODBC], native error numbers
- errors [ODBC], native error numbers
ms.assetid: 77cbc826-f47f-4803-8e7a-223d6df069b1
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: b8b9c46efdd901d8645f5c044105311041e7fa35
ms.sourcegitcommit: f3321ed29d6d8725ba6378d207277a57cb5fe8c2
ms.contentlocale: es-ES
ms.lasthandoff: 07/06/2020
ms.locfileid: "86009169"
---
# <a name="native-error-numbers"></a>Números de errores nativos
[!INCLUDE[SQL Server Azure SQL Database Synapse Analytics PDW ](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  En el caso de los errores que se producen en el origen de datos (devuelto por [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ), el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] controlador ODBC de Native Client devuelve el número de error nativo que devuelve [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] . En el caso de los errores detectados por el controlador, el [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] controlador ODBC de Native Client devuelve un número de error nativo de 0. Para obtener más información acerca de una lista de números de error nativos, vea la columna error de la tabla del sistema **sysmessages** en la base de datos **maestra** de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  
  
 Para obtener información acerca de los códigos de error de estado, consulte [SQLSTATE &#40;códigos de error ODBC&#41;](../../relational-databases/native-client-odbc-error-messages/sqlstate-odbc-error-codes.md). Para los errores devueltos por la Biblioteca de red, el número de error nativo es del software de red subyacente.  
  
## <a name="see-also"></a>Consulte también  
 [Controlar errores y mensajes](../../relational-databases/native-client-odbc-error-messages/handling-errors-and-messages.md)  
  
  
