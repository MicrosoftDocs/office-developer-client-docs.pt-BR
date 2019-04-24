---
title: Propriedade Recordset. Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bd9b91f80c9411bb7cdf4e0be9e71ab055dc72f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300620"
---
# <a name="recordsetbookmarkable-property-dao"></a>Propriedade Recordset. Bookmarkable (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna um valor que indica se um objeto **Recordset** suporta indicadores, que você pode definir usando a propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . Bookmarkable

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Verifique a definição da propriedade **Bookmarkable** de um objeto **Recordset** antes de você tentar definir ou verificar a propriedade **Bookmark**.

Para objetos **Recordset** com base em tabelas do mecanismo de banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é true, e você pode usar indicadores. No entanto, outros produtos do banco de dados podem não oferecer suporte aos marcadores. Por exemplo, não será possível usar os indicadores em qualquer objeto **Recordset** com base em uma tabela do Paradox vinculada que não tem chave primária.

## <a name="example"></a>Exemplo

Este exemplo utiliza as propriedades **Bookmark** e **Bookmarkable** para permitir que o usuário sinalize um registro no **Recordset** e volte a ele posteriormente.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
