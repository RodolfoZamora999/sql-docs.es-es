---
title: MSSQLSERVER_10061 | Microsoft Docs
description: El servidor no respondió a la solicitud del cliente en SQL Server. Vea una explicación del error y las posibles resoluciones.
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: language-reference
f1_keywords:
- "10061"
helpviewer_keywords:
- 10061 (Database Engine error)
ms.assetid: 729602f3-08df-474c-8740-8dea13c1eee3
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: cc775781dfce666ef663b2b3d36b4633524b30e5
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "85781542"
---
# <a name="mssqlserver_10061"></a>MSSQLSERVER_10061
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Detalles  
  
| Atributo | Value |  
| :-------- | :---- |  
|Nombre de producto|SQL Server|  
|Id. de evento|10061|  
|Origen de eventos|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico||  
|Texto del mensaje|Error al establecer una conexión al servidor.  La causa del problema en la conexión a SQL Server puede deberse a que SQL Server no permite conexiones remotas en su configuración predeterminada. (proveedor: Proveedor TCP, error: 0 - No se estableció ninguna conexión porque el equipo de destino la rechazó). (Microsoft SQL Server, Error: 10061)|  
  
## <a name="explanation"></a>Explicación  
El servidor no respondió a la solicitud del cliente. Este error puede producirse porque el servidor no se ha iniciado.  
  
## <a name="user-action"></a>Acción del usuario  
Asegúrese de que el servidor se haya iniciado.  
  
## <a name="see-also"></a>Consulte también  
[Administrar el servicio del motor de base de datos](~/database-engine/configure-windows/manage-the-database-engine-services.md)  
[Configurar protocolos de cliente](~/database-engine/configure-windows/configure-client-protocols.md)  
[Protocolos de red y bibliotecas de red](~/sql-server/install/network-protocols-and-network-libraries.md)  
[Configuración de red de cliente](~/database-engine/configure-windows/client-network-configuration.md)  
[Configurar protocolos de cliente](~/database-engine/configure-windows/configure-client-protocols.md)  
[Habilitar o deshabilitar un protocolo de red de servidor](~/database-engine/configure-windows/enable-or-disable-a-server-network-protocol.md)  
  
