---
title: Propriedade Recordset2.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7b0a086004d987a73e6dfb18fe5f919c239fb66c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700539"
---
# <a name="recordset2percentposition-property-dao"></a>Propriedade Recordset2.PercentPosition (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica o local aproximado do registro atual no objeto **[Recordset](recordset-object-dao.md)** com base em uma porcentagem de registros no **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* . PercentPosition

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Para indicar ou alterar a posição aproximada do registro atual em um objeto **Recordset**, você poderá verificar ou definir a propriedade **PercentPosition**. Quando você estiver trabalhando com um objeto **Recordset** do tipo dynaset ou instantâneo aberto diretamente a partir de uma tabela base, preencha primeiro o objeto **Recordset**, movendo-se para o último registro antes de definir ou verificar a propriedade **PercentPosition**. Se você usar a propriedade **PercentPosition** antes de preencher totalmente o objeto **Recordset**, a quantidade de movimento será relativa ao número de registros acessados, conforme indicado pela definição de propriedade **[RecordCount](recordset2-recordcount-property-dao.md)**. Você pode se mover para o último registro usando o método **[MoveLast](recordset2-movelast-method-dao.md)**.

> [!NOTE]
> Não é recomendável o uso da propriedade **PercentPosition** para mover o registro atual para um registro específico em um objeto **Recordset** . A propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** é a mais adequada para essa tarefa.

Assim que você definir a propriedade **PercentPosition** para um valor, o registro na posição aproximada que corresponder a esse valor se tornará o valor atual e a propriedade **PercentPosition** será redefinida para um valor que refletir a posição aproximada do registro atual. Por exemplo, se o objeto **Recordset** contiver somente cinco registros e você definir o valor da propriedade **PercentPosition** como 77, o valor retornado da propriedade **PercentPosition** poderá ser 80 e não 77.

A propriedade **PercentPosition** se aplica a todos os tipos de objetos **Recordset** , exceto os objetos **Recordset** tipo somente encaminhamento ou objetos **Recordset** abertos a partir de consultas passagem nos bancos de dados remotos.

Use a propriedade **PercentPosition** com uma barra de rolagem em um formulário ou uma caixa de texto para indicar o local do registro atual em um objeto **Recordset**.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **PercentPosition** para mostrar a posição do ponteiro do registro atual relativa ao início do **Recordset**.

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
