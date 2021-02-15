---
title: Filtragem de registros atualizados
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 791cbbd16eef7baf95fd51ab8624a04dc687166b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292395"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="7e22d-102">Filtragem de registros atualizados</span><span class="sxs-lookup"><span data-stu-id="7e22d-102">Filtering for updated records</span></span>

<span data-ttu-id="7e22d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e22d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="7e22d-104">Filtrando registros atualizados</span><span class="sxs-lookup"><span data-stu-id="7e22d-104">Filtering for Updated Records</span></span>

<span data-ttu-id="7e22d-p101">Antes de chamar **UpdateBatch**, você pode usar a propriedade **Filter** de **Recordset** para exibir somente os registros que foram alterados desde a abertura de **Recordset** ou da última chamada de **UpdateBatch**. Para isso, defina **Filter** como **adFilterPendingRecords** para determinar quantos registros serão atualizados, como mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="7e22d-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="7e22d-107">Este exemplo amplia o exemplo anterior de **UpdateBatch** filtrando o **Recordset** antes de chamar o **UpdateBatch**, mostrando ao usuário os registros que serão alterados e permitindo que ele cancele a atualização (usando o método **CancelBatch** ).</span><span class="sxs-lookup"><span data-stu-id="7e22d-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

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

