---
description: sp_rename (Transact-SQL)
title: sp_rename (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 01/09/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sp_rename_TSQL
- sp_rename
dev_langs:
- TSQL
helpviewer_keywords:
- renaming indexes
- renaming columns
- sp_rename
- renaming tables
ms.assetid: bc3548f0-143f-404e-a2e9-0a15960fc8ed
author: markingmyname
ms.author: maghan
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: edfe9a3a3d69c95b2a8778ca44583e005c6495c6
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89538661"
---
# <a name="sp_rename-transact-sql"></a>sp_rename (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

  Cambia el nombre de un objeto creado por el usuario en la base de datos actual. Este objeto puede ser una tabla, un índice, una columna, un tipo de datos de alias o un [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)] tipo definido por el usuario Common Language Runtime (CLR).  
  
> [!CAUTION]  
>  Al cambiar cualquier parte del nombre de un objeto se pueden interrumpir scripts y procedimientos almacenados. Se recomienda no utilizar esta instrucción para cambiar el nombre a procedimientos almacenados, desencadenadores, funciones definidas por el usuario o vistas; en su lugar, quite el objeto y vuelva a crearlo con el nuevo nombre.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
sp_rename [ @objname = ] 'object_name' , [ @newname = ] 'new_name'   
    [ , [ @objtype = ] 'object_type' ]   
```  
  
## <a name="arguments"></a>Argumentos  
 [ @objname =] '*object_name*'  
 Es el nombre actual completo o incompleto del objeto de usuario o tipo de datos. Si el objeto al que se va a cambiar el nombre es una columna de una tabla, *object_name* debe tener el formato *tabla. columna* o *esquema. tabla. columna*. Si el objeto cuyo nombre se va a cambiar es un índice, *object_name* debe tener el formato *TABLE. index* o *Schema. Table. index*. Si el objeto cuyo nombre se va a cambiar es una restricción, *object_name* debe tener el formato *Schema. Constraint*.  
  
 Las comillas solo se necesitan si se especifica un objeto completo. Si se proporciona un nombre completo, incluido el nombre de la base de datos, el nombre de la base de datos debe ser el de la base de datos actual. *object_name* es de tipo **nvarchar (776)** y no tiene ningún valor predeterminado.  
  
 [ @newname =] '*new_name*'  
 Es el nuevo nombre del objeto especificado. *new_name* debe ser un nombre de una parte y debe cumplir las reglas de los identificadores. *NewName* es de **tipo sysname**y no tiene ningún valor predeterminado.  
  
> [!NOTE]  
>  Los nombres de los desencadenadores no pueden comenzar por # o ##.  
  
 [ @objtype =] '*object_type*'  
 Es el tipo de objeto cuyo nombre se va a cambiar. *object_type* es de tipo **VARCHAR (13)**, su valor predeterminado es NULL y puede tener uno de estos valores.  
  
|Valor|Descripción|  
|-----------|-----------------|  
|COLUMN|Una columna cuyo nombre se va a cambiar.|  
|DATABASE|Una base de datos definida por el usuario. Este tipo de objeto es necesario cuando se cambia el nombre de una base de datos|  
|INDEX|Índice definido por el usuario. Si se cambia el nombre a un índice con estadísticas, también se cambia automáticamente a las estadísticas.|  
|OBJECT|Un elemento de un tipo del que se realiza un seguimiento en [Sys. Objects](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md). Por ejemplo, OBJECT podría utilizarse para cambiar el nombre de objetos como restricciones (CHECK, FOREIGN KEY, PRIMARY o UNIQUE KEY), tablas de usuario y reglas.|  
|STATISTICS|**Se aplica a**: [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] y versiones posteriores, y [!INCLUDE[ssSDSfull](../../includes/sssdsfull-md.md)]<br /><br /> Estadísticas que crea un usuario explícitamente o que se crean implícitamente con un índice. Si se cambia el nombre de las estadísticas de un índice, también se cambia automáticamente el nombre del índice.|  
|USERDATATYPE|[Tipos definidos por el usuario CLR](../../relational-databases/clr-integration-database-objects-user-defined-types/clr-user-defined-types.md) agregados al ejecutar [CREATE Type](../../t-sql/statements/create-type-transact-sql.md) o [sp_addtype](../../relational-databases/system-stored-procedures/sp-addtype-transact-sql.md).|  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 0 (correcto) o un número distinto de cero (error)  
  
## <a name="remarks"></a>Observaciones  
 Solo se puede cambiar el nombre de un objeto o tipo de datos de la base de datos actual. No se pueden cambiar los nombres de la mayoría de los tipos de datos y objetos del sistema.  
  
 sp_rename cambia automáticamente el nombre del índice asociado cuando se cambia el nombre de una restricción PRIMARY KEY o UNIQUE. Si un índice cuyo nombre se ha cambiado está enlazado a una restricción PRIMARY KEY, sp_rename también cambia automáticamente el nombre de esta restricción.  
  
 sp_rename se puede utilizar para cambiar el nombre de los índices XML principales y secundarios.  
  
 Al cambiar el nombre de un procedimiento almacenado, una función, una vista o un desencadenador, no se cambiará el nombre del objeto correspondiente en la columna de definición de la vista de catálogo [Sys. sql_modules](../../relational-databases/system-catalog-views/sys-sql-modules-transact-sql.md) u obtenida mediante la función integrada [OBJECT_DEFINITION](../../t-sql/functions/object-definition-transact-sql.md) . Por lo tanto, se recomienda no utilizar sp_rename para cambiar el nombre a estos tipos de objetos. En su lugar, quite el objeto y vuelva a crearlo con su nuevo nombre.  
  
 Al cambiar el nombre de un objeto como una tabla o columna, no se cambia automáticamente el nombre de las referencias a ese objeto. Es necesario modificar de forma manual los objetos que hacen referencia al objeto cuyo nombre se ha cambiado. Por ejemplo, si se cambia el nombre de una columna de una tabla y en un desencadenador existe una referencia a esa columna, es necesario modificar el desencadenador para reflejar el nuevo nombre de la columna. Use [sys.sql_expression_dependencies](../../relational-databases/system-catalog-views/sys-sql-expression-dependencies-transact-sql.md) para ver las dependencias del objeto antes de cambiarle el nombre.  
  
## <a name="permissions"></a>Permisos  
 Para cambiar el nombre de objetos, columnas e índices, se necesita permiso ALTER en el objeto. Para cambiar el nombre de tipos de usuario, se necesita el permiso CONTROL en el tipo. Para cambiar el nombre de una base de datos, debe pertenecer a los roles fijos de servidor sysadmin o dbcreator.   
  
## <a name="examples"></a>Ejemplos  
  
### <a name="a-renaming-a-table"></a>A. Cambiar el nombre de una tabla  
 En el siguiente ejemplo se cambia el nombre de la tabla `SalesTerritory` por `SalesTerr` en el esquema `Sales` .  
  
```  
USE AdventureWorks2012;  
GO  
EXEC sp_rename 'Sales.SalesTerritory', 'SalesTerr';  
GO  
```  
  
### <a name="b-renaming-a-column"></a>B. Cambiar el nombre de una columna  
 En el ejemplo siguiente se cambia el nombre de la `TerritoryID` columna de la `SalesTerritory` tabla a `TerrID` .  
  
```  
USE AdventureWorks2012;  
GO  
EXEC sp_rename 'Sales.SalesTerritory.TerritoryID', 'TerrID', 'COLUMN';  
GO  
```  
  
### <a name="c-renaming-an-index"></a>C. Cambiar el nombre de un índice  
 En el siguiente ejemplo se cambia el nombre del índice `IX_ProductVendor_VendorID` por `IX_VendorID`.  
  
```  
USE AdventureWorks2012;  
GO  
EXEC sp_rename N'Purchasing.ProductVendor.IX_ProductVendor_VendorID', N'IX_VendorID', N'INDEX';  
GO  
```  
  
### <a name="d-renaming-an-alias-data-type"></a>D. Cambiar el nombre de un tipo de datos de alias  
 En el siguiente ejemplo se cambia el nombre del tipo de datos de alias `Phone` por `Telephone`.  
  
```  
USE AdventureWorks2012;  
GO  
EXEC sp_rename N'Phone', N'Telephone', N'USERDATATYPE';  
GO  
```  
  
### <a name="e-renaming-constraints"></a>E. Cambiar el nombre de las restricciones  
 En los siguientes ejemplos se cambia el nombre de las restricciones PRIMARY KEY, CHECK y FOREIGN KEY. Al cambiar el nombre de una restricción, debe especificarse el esquema al que pertenece.  
  
```  
USE AdventureWorks2012;   
GO  
-- Return the current Primary Key, Foreign Key and Check constraints for the Employee table.  
SELECT name, SCHEMA_NAME(schema_id) AS schema_name, type_desc  
FROM sys.objects  
WHERE parent_object_id = (OBJECT_ID('HumanResources.Employee'))   
AND type IN ('C','F', 'PK');   
GO  
  
-- Rename the primary key constraint.  
sp_rename 'HumanResources.PK_Employee_BusinessEntityID', 'PK_EmployeeID';  
GO  
  
-- Rename a check constraint.  
sp_rename 'HumanResources.CK_Employee_BirthDate', 'CK_BirthDate';  
GO  
  
-- Rename a foreign key constraint.  
sp_rename 'HumanResources.FK_Employee_Person_BusinessEntityID', 'FK_EmployeeID';  
  
-- Return the current Primary Key, Foreign Key and Check constraints for the Employee table.  
SELECT name, SCHEMA_NAME(schema_id) AS schema_name, type_desc  
FROM sys.objects  
WHERE parent_object_id = (OBJECT_ID('HumanResources.Employee'))   
AND type IN ('C','F', 'PK');  
  
```  
  
```  
  
name                                  schema_name        type_desc  
------------------------------------- ------------------ ----------------------  
FK_Employee_Person_BusinessEntityID   HumanResources     FOREIGN_KEY_CONSTRAINT  
PK_Employee_BusinessEntityID          HumanResources     PRIMARY_KEY_CONSTRAINT  
CK_Employee_BirthDate                 HumanResources     CHECK_CONSTRAINT  
CK_Employee_MaritalStatus             HumanResources     CHECK_CONSTRAINT  
CK_Employee_HireDate                  HumanResources     CHECK_CONSTRAINT  
CK_Employee_Gender                    HumanResources     CHECK_CONSTRAINT  
CK_Employee_VacationHours             HumanResources     CHECK_CONSTRAINT  
CK_Employee_SickLeaveHours            HumanResources     CHECK_CONSTRAINT  
  
(7 row(s) affected)  
  
name                                  schema_name        type_desc  
------------------------------------- ------------------ ----------------------  
FK_Employee_ID                        HumanResources     FOREIGN_KEY_CONSTRAINT  
PK_Employee_ID                        HumanResources     PRIMARY_KEY_CONSTRAINT  
CK_BirthDate                          HumanResources     CHECK_CONSTRAINT  
CK_Employee_MaritalStatus             HumanResources     CHECK_CONSTRAINT  
CK_Employee_HireDate                  HumanResources     CHECK_CONSTRAINT  
CK_Employee_Gender                    HumanResources     CHECK_CONSTRAINT  
CK_Employee_VacationHours             HumanResources     CHECK_CONSTRAINT  
CK_Employee_SickLeaveHours            HumanResources     CHECK_CONSTRAINT  
  
(7 row(s) affected)  
  
```  
  
### <a name="f-renaming-statistics"></a>F. Cambiar el nombre de las estadísticas  
 En el ejemplo siguiente se crea un objeto de estadísticas denominado contactMail1 y, a continuación, se cambia el nombre de la estadística a NewContact mediante sp_rename. Al cambiar el nombre de las estadísticas, el objeto se debe especificar con el formato schema.table.statistics_name.  
  
```  
CREATE STATISTICS ContactMail1  
    ON Person.Person (BusinessEntityID, EmailPromotion)  
    WITH SAMPLE 5 PERCENT;  
  
sp_rename 'Person.Person.ContactMail1', 'NewContact','Statistics';  
  
```  
  
## <a name="see-also"></a>Consulte también  
 [sys.sql_expression_dependencies &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-sql-expression-dependencies-transact-sql.md)   
 [sys.sql_modules &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-sql-modules-transact-sql.md)   
 [Procedimientos almacenados del sistema &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)   
 [Motor de base de datos procedimientos almacenados &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/database-engine-stored-procedures-transact-sql.md)  
  
  
