---
title: Filtrando registros atualizados
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3bf6619b9b375642bc9f279aea92cb20df3b859
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947809"
---
# <a name="filtering-for-updated-records"></a>Filtrando registros atualizados

**Aplica-se a**: Access 2013, o Office 2013

## <a name="filtering-for-updated-records"></a>Filtragem de registros atualizados

Antes de chamar **UpdateBatch**, você pode usar a propriedade **Filter** de **Recordset** para exibir somente os registros que foram alterados desde a abertura de **Recordset** ou da última chamada de **UpdateBatch**. Para isso, defina **Filter** como **adFilterPendingRecords** para determinar quantos registros serão atualizados, como mostrado abaixo.

Este exemplo amplia o exemplo anterior de **UpdateBatch** filtrando o **Recordset** antes de chamar o **UpdateBatch**, mostrando ao usuário os registros que serão alterados e permitindo que ele cancele a atualização (usando o método **CancelBatch** ).

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```

