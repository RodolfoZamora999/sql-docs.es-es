---
description: 'Paso 4: Relleno del cuadro de texto de detalles'
title: 'Paso 4: rellenar el cuadro de texto de detalles | Microsoft Docs'
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
ms.assetid: cb4273e2-c907-4a86-a621-3bf110088228
author: rothja
ms.author: jroth
ms.openlocfilehash: 868066b8225a3e87a2aad37ddd7569cc5be6bd75
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88979486"
---
# <a name="step-4-populate-the-details-text-box"></a>Paso 4: Relleno del cuadro de texto de detalles
Para rellenar el cuadro de texto detalles, cree una nueva subrutina denominada **recFields** e inserte el código siguiente:  
  
```  
Sub recFields(r As Record, l As ListBox, t As TextBox)  
    Dim f As Field  
    Dim s As Stream  
    Set s = New Stream  
    Dim str As String  
  
    For Each f In r.Fields  
        l.AddItem f.Name & ": " & f.Value  
    Next  
    t.Text = ""  
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then  
        s.Open r, adModeRead, adOpenStreamFromRecord  
        str = s.ReadText(1)  
        s.Position = 0  
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?"  
            s.Charset = "ascii"  
            s.Type = adTypeText  
        End If  
        t.Text = s.ReadText(adReadAll)  
    End If  
End Sub  
```  
  
 Este código se rellena `lstDetails` con los campos y valores del registro simple que se pasa a `recFields` . Si el recurso es un archivo de texto, se abre una secuencia de texto desde el registro de recursos. El código determina si el juego de caracteres es ASCII y copia el contenido de la secuencia en `txtDetails` .  
  
## <a name="see-also"></a>Consulte también  
 [Escenario de publicación en Internet](../../../ado/guide/data/internet-publishing-scenario.md)   
 [Paso 3: Relleno del cuadro de lista de campos](../../../ado/guide/data/step-3-populate-the-fields-list-box.md)
