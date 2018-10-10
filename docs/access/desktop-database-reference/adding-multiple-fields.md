---
title: Adicionando vários campos
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9bca4035917f4376ccf69201d79894a0273ceb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464001"
---
# <a name="adding-multiple-fields"></a>Adicionando vários campos


**Aplica-se a**: Access 2013 | Office 2013

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

