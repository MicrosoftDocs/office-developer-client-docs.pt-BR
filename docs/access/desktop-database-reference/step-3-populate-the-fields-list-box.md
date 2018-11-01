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
# <a name="step-3-populate-the-fields-list-box"></a>Etapa 3: Preencher a caixa de listagem Campos


**Aplica-se a**: Access 2013, o Office 2013

## <a name="step-3-populate-the-fields-list-box"></a>Etapa 3: Preencher a caixa de listagem de campos

**Para preencher a caixa de texto Campos**

Insira o seguinte código no manipulador de eventos Click de lstMain:

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

Este código declara e instancia os locais de **registro** e objetos **Recordset** , rec e e rs, respectivamente.

A linha correspondente ao recurso selecionado em lstMain é feita na linha atual de grs. Em seguida, caixa de listagem **detalhes** é desmarcada e rec é aberto com a linha atual de. Em seguida, caixa de listagem **detalhes** é desmarcada e rec é aberto com a linha atual de grs como a fonte.

Se o recurso for um registro de coleção (conforme especificado por **RecordType**), o local **Recordset**, rs, é aberto nos filhos de rec. Em seguida, lstDetails é preenchido com os valores das linhas de é aberto nos filhos de rec. Em seguida, lstDetails é preenchido com os valores das linhas de rs.

Se o recurso for um registro simples, recFields será chamado. Para obter mais informações sobre recFields, consulte a próxima etapa.

Nenhum código será implementado se o recurso for um documento estruturado.

