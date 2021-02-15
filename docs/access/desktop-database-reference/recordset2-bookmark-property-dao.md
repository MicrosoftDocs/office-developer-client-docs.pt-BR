---
title: Propriedade Recordset2.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31791e9fb3c7081989232e36a90b184ed7e31866
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307445"
---
# <a name="recordset2bookmark-property-dao"></a>Propriedade Recordset2.Bookmark (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um marcador que identifica exclusivamente o registro atual em um objeto **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* .Bookmark

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Para um **objeto Recordset** baseado inteiramente nas tabelas do mecanismo de banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é True e você pode usar a propriedade **Bookmark** com esse recordset. No entanto, outros produtos do banco de dados podem não oferecer suporte aos marcadores. Por exemplo, não é possível usar marcadores em nenhum objeto **Recordset2** com base em uma tabela Paradox vinculada que não tem chave primária.

Quando você criar ou abrir um objeto **Recordset**, cada um desses registros já possuirá um marcador exclusivo. Salve o marcador do registro atual pela atribuição do valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente ao registro a qualquer momento depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** como o valor dessa variável.

Não há limite para o número de marcadores que você pode estabelecer. Para criar um marcador de um registro diferente do registro atual, mova-se para o registro desejado e atribua o valor da propriedade **Bookmark** a uma variável **String** que identifique o registro.

Para garantir que o objeto **Recordset** seja compatível com marcadores, verifique os valores de sua propriedade **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** antes de usar a propriedade **Bookmark**. Se a propriedade **Bookmarkable** for False, o objeto **Recordset** não oferecerá suporte aos marcadores e usará os resultados da propriedade **Bookmark** em um erro interceptável.

Se você usar o método **[Clone](recordset2-clone-method-dao.md)** para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** dos objetos **Recordset** original e duplicado serão idênticas e poderão ser usadas de forma permutável. No entanto, você não pode usar marcadores de objetos **Recordset** diferentes de forma permutável, mesmo que esses marcadores tenham sido criados usando o mesmo objeto ou a mesma instrução SQL.

Se você definir a propriedade **Bookmark** como um valor que representa um registro excluído, ocorrerá um erro interceptável.

O valor da propriedade **Bookmark** Bookmark não é o mesmo que um número de registro.

## <a name="example"></a>Exemplo

Este exemplo usa as propriedades **Bookmark** e **Bookmarkable** para permitir que o usuário sinalize um registro em um conjunto de registros e retorne mais tarde.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
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

<br/>

Este exemplo usa a propriedade **LastModified** para mover o ponteiro do registro atual para o registro modificado e para o registro recentemente criado.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
