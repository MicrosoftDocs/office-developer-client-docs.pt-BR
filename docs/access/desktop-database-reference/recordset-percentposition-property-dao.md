---
title: Propriedade Recordset.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5793d2b73e424726e91cf3bbb54b09db59123b92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463534"
---
# <a name="recordsetpercentposition-property-dao"></a>Propriedade Recordset.PercentPosition (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que indica o local aproximado do registro atual no objeto **[Recordset](recordset-object-dao.md)** com base em uma porcentagem de registros no **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* . PercentPosition

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Para indicar ou alterar a posição aproximada do registro atual em um objeto **Recordset**, você poderá verificar ou definir a propriedade **PercentPosition**. Quando você estiver trabalhando com um objeto **Recordset** do tipo dynaset ou instantâneo aberto diretamente a partir de uma tabela base, preencha primeiro o objeto **Recordset**, movendo-se para o último registro antes de definir ou verificar a propriedade **PercentPosition**. Se você usar a propriedade **PercentPosition** antes de preencher totalmente o objeto **Recordset**, a quantidade de movimento será relativa ao número de registros acessados, conforme indicado pela definição de propriedade **[RecordCount](recordset-recordcount-property-dao.md)**. Você pode se mover para o último registro usando o método **[MoveLast](recordset-movelast-method-dao.md)**.


> [!NOTE]
> <P>[!OBSERVAçãO] O uso da propriedade <STRONG>PercentPosition</STRONG> para mover o registro atual para um registro específico em um objeto <STRONG>Recordset</STRONG> não é recomendável? A propriedade <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> é a mais adequada para essa tarefa.</P>



Assim que você definir a propriedade **PercentPosition** para um valor, o registro na posição aproximada que corresponder a esse valor se tornará o valor atual e a propriedade **PercentPosition** será redefinida para um valor que refletir a posição aproximada do registro atual. Por exemplo, se o objeto **Recordset** contiver somente cinco registros e você definir o valor da propriedade **PercentPosition** como 77, o valor retornado da propriedade **PercentPosition** poderá ser 80 e não 77.

A propriedade **PercentPosition** se aplica a todos os tipos de objetos **Recordset** , exceto os objetos **Recordset** tipo somente encaminhamento ou objetos **Recordset** abertos a partir de consultas passagem nos bancos de dados remotos.

Use a propriedade **PercentPosition** com uma barra de rolagem em um formulário ou uma caixa de texto para indicar o local do registro atual em um objeto **Recordset**.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **PercentPosition** para mostrar a posição do ponteiro do registro atual relativa ao início do **Recordset**.

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
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
