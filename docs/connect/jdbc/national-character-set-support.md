---
description: Compatibilidad con juegos de caracteres nacionales
title: Compatibilidad con juegos de caracteres nacionales | Microsoft Docs
ms.custom: ''
ms.date: 08/12/2019
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: 4fceacfd-df4f-40cd-b7a2-5e5e58a5979f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 394d81f28921bfc4e68204778ed6fcdf1e2fb9e7
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88438347"
---
# <a name="national-character-set-support"></a>Compatibilidad con juegos de caracteres nacionales
[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

  El controlador JDBC proporciona compatibilidad con la API de JDBC 4.0, que incluye nuevos métodos de la API de conversión de juegos de caracteres nacionales. Esta compatibilidad incluye nuevos métodos establecedor, captador y actualizador para los tipos de JDBC **NCHAR**, **NVARCHAR**, **LONGNVARCHAR** y **NCLOB**.  
  
 A continuación se incluye una lista de nuevos métodos captador, establecedor y actualizador que permiten la conversión al juego de caracteres nacionales:  
  
-   [SQLServerPreparedStatement](../../connect/jdbc/reference/sqlserverpreparedstatement-class.md): [setNString](../../connect/jdbc/reference/setnstring-method-int-java-lang-string.md), [setNCharacterStream](../../connect/jdbc/reference/setncharacterstream-method-sqlserverpreparedstatement.md), [setNClob](../../connect/jdbc/reference/setnclob-method-sqlserverpreparedstatement.md).  
  
-   [SQLServerCallableStatement](../../connect/jdbc/reference/sqlservercallablestatement-class.md): [getNClob](../../connect/jdbc/reference/getnclob-method-sqlservercallablestatement.md), [getNString](../../connect/jdbc/reference/getnstring-method-sqlservercallablestatement.md), [getNCharacterStream](../../connect/jdbc/reference/getncharacterstream-method-sqlservercallablestatement.md), [setNString](../../connect/jdbc/reference/setnstring-method-sqlservercallablestatement.md), [setNCharacterStream](../../connect/jdbc/reference/setncharacterstream-method-sqlservercallablestatement.md), [setNClob](../../connect/jdbc/reference/setnclob-method-sqlservercallablestatement.md).  
  
-   [SQLServerResultSet](../../connect/jdbc/reference/sqlserverresultset-class.md): [getNClob](../../connect/jdbc/reference/getnclob-method-sqlserverresultset.md), [getNString](../../connect/jdbc/reference/getnstring-method-sqlserverresultset.md), [getNCharacterStream](../../connect/jdbc/reference/getncharacterstream-method-sqlserverresultset.md), [updateNClob](../../connect/jdbc/reference/updatenclob-method-sqlserverresultset.md), [updateNString](../../connect/jdbc/reference/updatenstring-method-sqlserverresultset.md), [updateNCharacterStream](../../connect/jdbc/reference/updatencharacterstream-method-sqlserverresultset.md).  
  
> [!NOTE]  
>  Para usar estos métodos en su aplicación, debe establecer la ruta de clase para incluir el archivo sqljdbc4.jar.  
  
 Para enviar formatos String al servidor en el formato Unicode, las aplicaciones deberían o bien usar los nuevos métodos de carácter nacional de JDBC 4.0 o bien establecer la propiedad de la conexión **sendStringParametersAsUnicode** en **true** cuando se usan métodos de caracteres no nacionales. Lo recomendable es usar los nuevos métodos de caracteres nacionales de JDBC 4.0 cuando sea posible. Para obtener más información sobre la propiedad de conexión **sendStringParametersAsUnicode**, consulte [Establecimiento de las propiedades de conexión](../../connect/jdbc/setting-the-connection-properties.md).  
  
## <a name="see-also"></a>Consulte también  
 [Descripción de los tipos de datos del controlador JDBC](../../connect/jdbc/understanding-the-jdbc-driver-data-types.md)  
  
  
