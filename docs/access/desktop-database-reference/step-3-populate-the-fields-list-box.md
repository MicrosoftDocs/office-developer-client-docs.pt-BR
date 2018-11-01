---
title: 'Etapa 3: Preencher a caixa de listagem Campos'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae1513c47c79da4f4df7fee2f3f3d7b3507ac1c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876656"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="0b256-102">Etapa 3: Preencher a caixa de listagem Campos</span><span class="sxs-lookup"><span data-stu-id="0b256-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="0b256-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b256-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="0b256-104">Etapa 3: Preencher a caixa de listagem de campos</span><span class="sxs-lookup"><span data-stu-id="0b256-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="0b256-105">**Para preencher a caixa de texto Campos**</span><span class="sxs-lookup"><span data-stu-id="0b256-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="0b256-106">Insira o seguinte código no manipulador de eventos Click de lstMain:</span><span class="sxs-lookup"><span data-stu-id="0b256-106">Insert the following code into the Click event handler of lstMain:</span></span>

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

<span data-ttu-id="0b256-107">Este código declara e instancia os locais de **registro** e objetos **Recordset** , rec e e rs, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0b256-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="0b256-108">A linha correspondente ao recurso selecionado em lstMain é feita na linha atual de grs.</span><span class="sxs-lookup"><span data-stu-id="0b256-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="0b256-109">Em seguida, caixa de listagem **detalhes** é desmarcada e rec é aberto com a linha atual de.</span><span class="sxs-lookup"><span data-stu-id="0b256-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="0b256-110">Em seguida, caixa de listagem **detalhes** é desmarcada e rec é aberto com a linha atual de grs como a fonte.</span><span class="sxs-lookup"><span data-stu-id="0b256-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="0b256-111">Se o recurso for um registro de coleção (conforme especificado por **RecordType**), o local **Recordset**, rs, é aberto nos filhos de rec. Em seguida, lstDetails é preenchido com os valores das linhas de é aberto nos filhos de rec. Em seguida, lstDetails é preenchido com os valores das linhas de rs.</span><span class="sxs-lookup"><span data-stu-id="0b256-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="0b256-p102">Se o recurso for um registro simples, recFields será chamado. Para obter mais informações sobre recFields, consulte a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="0b256-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="0b256-114">Nenhum código será implementado se o recurso for um documento estruturado.</span><span class="sxs-lookup"><span data-stu-id="0b256-114">No code is implemented if the resource is a structured document.</span></span>

