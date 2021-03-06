---
title: Habilitación o deshabilitación de la recopilación de datos de uso y los informes de bloqueo
description: En este artículo se explica cómo controlar si se recopilan datos de informes de uso y de bloqueo y se envían a Microsoft.
ms.prod: azure-data-studio
ms.technology: azure-data-studio
ms.topic: how-to
author: markingmyname
ms.author: maghan
ms.reviewer: alayu, maghan, sstein
ms.custom: seodec18; seo-lt-2019
ms.date: 09/24/2018
ms.openlocfilehash: 5ef44a7e2981d98c749e25692e667ae71b42843d
ms.sourcegitcommit: 63aef5a96905f0b026322abc9ccb862ee497eebe
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2020
ms.locfileid: "91363892"
---
# <a name="enable-or-disable-usage-data-collection-for-azure-data-studio"></a>Habilitación o deshabilitación de la recopilación de datos de uso para Azure Data Studio

## <a name="how-to-disable-telemetry-reporting"></a>Cómo deshabilitar los informes de telemetría

Azure Data Studio recopila datos de uso y los envía a Microsoft para ayudar a mejorar los productos y servicios. Para obtener más información, vea la [declaración de privacidad](https://go.microsoft.com/fwlink/?LinkID=528096&clcid=0x409).

Si no quiere enviar datos de uso a Microsoft, puede establecer el valor *telemetry.enableTelemetry* en *false*.

Para silenciar todos los eventos de telemetría de Azure Data Studio, en **Archivo** > **Preferencias** > **Configuración**, agregue la opción siguiente:

```json
    "telemetry.enableTelemetry": false
```

**Aviso importante**: Esta opción requiere que se reinicie Azure Data Studio para surtir efecto. 

## <a name="how-to-disable-crash-reporting"></a>Cómo deshabilitar los informes de bloqueo

Para deshabilitar los informes de bloqueo, en **Archivo** > **Preferencias** > **Configuración**, agregue la siguiente opción:

```json
    "telemetry.enableCrashReporter": false
```

**Aviso importante**: Esta opción requiere que se reinicie Azure Data Studio para surtir efecto.

## <a name="additional-resources"></a>Recursos adicionales
- [Configuración de área de trabajo y usuario](settings.md)
