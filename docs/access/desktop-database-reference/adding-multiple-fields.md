---
title: Adicionando vários campos
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01330eeed2645a0bd76f6ac51e96542068b245e7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878973"
---
# <a name="adding-multiple-fields"></a>Adicionando vários campos


**Aplica-se a**: Access 2013, o Office 2013

Às vezes, pode ser mais eficiente passar uma matriz de campos e seus valores correspondentes para o método **AddNew**, em vez de definir **Value** várias vezes para cada novo campo. Se *FieldList* é uma matriz, os *valores* também deve ser uma matriz com o mesmo número de membros; Caso contrário, ocorrerá um erro. A ordem dos nomes de campo deve corresponder à ordem dos valores de campo em cada matriz. O código a seguir passa uma matriz de campos e uma matriz de valores para o método **AddNew**.

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

