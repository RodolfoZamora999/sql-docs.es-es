---
description: '&#x40;&#x40;LOCK_TIMEOUT (Transact-SQL)'
title: '@@LOCK_TIMEOUT (Transact-SQL) | Microsoft Docs'
ms.custom: ''
ms.date: 09/19/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- '@@LOCK_TIMEOUT'
- '@@LOCK_TIMEOUT_TSQL'
dev_langs:
- TSQL
helpviewer_keywords:
- timeout options [SQL Server], locks
- '@@LOCK_TIMEOUT function'
- current lock time-out setting
- locking [SQL Server], time-outs
ms.assetid: 6bf8bf97-60b8-40c1-b89d-8f5a00bcae2e
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 8344739fb058956f95367bb190132cec57a28923
ms.sourcegitcommit: cc23d8646041336d119b74bf239a6ac305ff3d31
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2020
ms.locfileid: "91115506"
---
# <a name="x40x40lock_timeout-transact-sql"></a>&#x40;&#x40;LOCK_TIMEOUT (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

  Devuelve el valor actual de tiempo de espera de bloqueo en milisegundos para la sesión actual.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```syntaxsql  
@@LOCK_TIMEOUT  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-types"></a>Tipos de valor devuelto
 **integer**  
  
## <a name="remarks"></a>Comentarios  
 SET LOCK_TIMEOUT permite a una aplicación establecer el tiempo máximo que espera una instrucción en un recurso bloqueado. Cuando una instrucción ha esperado más tiempo que el indicado en LOCK_TIMEOUT, la instrucción bloqueada se cancela automáticamente y se devuelve un mensaje de error a la aplicación.  
  
 @@LOCK_TIMEOUT devuelve un valor de -1 si SET LOCK_TIMEOUT aún no se ha ejecutado en la sesión actual.  
  
## <a name="examples"></a>Ejemplos  
 En este ejemplo se muestra el conjunto de resultados cuando no se establece un valor en LOCK_TIMEOUT.  
  
```sql  
SELECT @@LOCK_TIMEOUT AS [Lock Timeout];  
GO  
```  
  
 El conjunto de resultados es:  
  
```  
Lock Timeout  
------------  
-1  
```  
  
 En este ejemplo se establece LOCK_TIMEOUT en 1800 milisegundos y, luego, se llama a @@LOCK_TIMEOUT.  
  
```sql  
SET LOCK_TIMEOUT 1800;  
SELECT @@LOCK_TIMEOUT AS [Lock Timeout];  
GO  
```  
  
 El conjunto de resultados es:  
  
```  
Lock Timeout  
------------  
1800          
```  
  
## <a name="see-also"></a>Vea también  
 [Funciones de configuración &#40;Transact-SQL&#41;](../../t-sql/functions/configuration-functions-transact-sql.md)   
 [SET LOCK_TIMEOUT &#40;Transact-SQL&#41;](../../t-sql/statements/set-lock-timeout-transact-sql.md)  
  
  
