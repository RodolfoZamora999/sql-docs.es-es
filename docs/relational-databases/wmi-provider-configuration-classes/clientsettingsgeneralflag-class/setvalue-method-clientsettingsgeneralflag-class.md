---
description: Método SetValue (clase ClientSettingsGeneralFlag)
title: Método SetValue (ClientSettingsGeneralFlag)
ms.custom: seo-lt-2019
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: wmi
ms.topic: reference
apiname:
- SetValue Method (ClientSettingsGeneralFlag Class)
apilocation:
- sqlmgmproviderxpsp2up.mof
apitype: MOFDef
helpviewer_keywords:
- SetValue method
ms.assetid: 34443689-a0e0-4668-a811-17532c6fd271
author: markingmyname
ms.author: maghan
ms.openlocfilehash: b2475eac5044c28b3f5a5a52037ac1a3e0715a0c
ms.sourcegitcommit: 783b35f6478006d654491cb52f6edf108acf2482
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "91892525"
---
# <a name="setvalue-method-clientsettingsgeneralflag-class"></a>Método SetValue (clase ClientSettingsGeneralFlag)
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sqlserver.md)]
  Establece todos los valores de la marca a la que se hace referencia.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
object.SetValue(Value)  
```  
  
## <a name="parts"></a>Partes  
 *object*  
 Objeto de la [clase ClientSettingsGeneralFlag](../../../relational-databases/wmi-provider-configuration-classes/clientsettingsgeneralflag-class/clientsettingsgeneralflag-class.md) que representa una marca general para la configuración del servidor.  
  
#### <a name="parameters"></a>Parámetros  
  
|Parámetro|Descripción|  
|---------------|-----------------|  
|*Valor*|Valor booleano que especifica el valor de la marca.|  
  
## <a name="property-valuereturn-value"></a>Valor de propiedad y valor devuelto  
 Valor **uint32** que es 0 si se modificó el servicio correctamente, 1 si no se admite la solicitud y cualquier otro número para indicar un error.  
  
## <a name="remarks"></a>Comentarios  
  
## <a name="see-also"></a>Consulte también  
 [Configurar protocolos de cliente](../../../database-engine/configure-windows/configure-client-protocols.md)  
  
