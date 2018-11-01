---
title: Propriedade Recordset.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 644eb2e1a8f979451d233bcc5a48f723c25739b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888472"
---
# <a name="recordsetbookmark-property-dao"></a>Propriedade Recordset.Bookmark (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um Bookmark que identifica exclusivamente o registro atual em um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . Indicador

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Para um objeto **Recordset** baseado inteiramente em tabelas de mecanismo de banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é True e você pode usar a propriedade **Bookmark** com esse **conjunto de registros**. Entretanto, outros produtos de banco de dados podem não aceitar indicadores. Por exemplo, você não pode usar indicadores em nenhum objeto **Recordset** com base em uma tabela vinculada Paradox que não tenha nenhuma chave primária.

Quando você cria ou abre um objeto **Recordset**, cada um de seus registros já tem um indicador exclusivo. Você pode salvar o indicador para o registro atual, atribuindo o valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente para aquele registro em qualquer momento depois de mover-se para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** para o valor daquela variável.

Não há limite no número de indicadores que podem ser estabelecidos. Para criar um indicador de um registro que não seja o atual, mova para o registro desejado e atribua o valor da propriedade **Bookmark** a uma variável **String** que identifique esse registro.

Para confirmar se o objeto **Recordset** aceita indicadores, verifique o valor de sua propriedade **[Bookmarkable](recordset-bookmarkable-property-dao.md)** antes de usar a propriedade **Bookmark**. Se a propriedade **Bookmarkable** for False, o objeto **Recordset** não oferece suporte a indicadores e usando o **indicador** de propriedade resulta em um erro interceptável.

Se você usar o método **[Clone](recordset-clone-method-dao.md)** para criar uma cópia de um objeto **Recordset**, as configurações da propriedade **Bookmark** para os objetos **Recordset** originais e duplicados serão idênticas e poderão ser utilizadas de modo intercambiável. Entretanto, você não poderá usar indicadores de objetos **Recordset** diferentes desse modo, mesmo se eles tiverem sido criados com o uso do mesmo objeto ou da mesma instrução SQL.

Se você usar a propriedade **Bookmark** para um valor que represente um registro excluído, ocorrerá um erro interceptável.

O valor da propriedade **Bookmark**Bookmark não é o mesmo que um número de registro.

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

<br/>

Este exemplo usa a propriedade **LastModified** para mover o ponteiro do registro atual para o registro modificado e para o registro recentemente criado.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
