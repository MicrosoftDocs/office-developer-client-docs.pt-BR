---
title: Método Recordset.Update (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d81eaf181a87d6afc13dbf2908be307d120d349
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997018"
---
# <a name="recordsetupdate-method-dao"></a>Método Recordset.Update (DAO)

**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Atualização (***UpdateType***, ***Force***)

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Uma constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> indicando o tipo de atualização, como especificado em Configurações (somente espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Um valor <strong>Boolean</strong> indicando se é preciso impor ou não as alterações ao banco de dados, independentemente de os dados subjacentes terem sido alterados por outro usuário desde a chamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Se for <strong>True</strong>, as alterações serão impostas e as alterações feitas por outros usuários serão simplesmente substituídas. Se for <strong>False</strong> (padrão), as alterações feitas por outro usuário enquanto a atualização estiver pendente causarão uma falha na atualização para as alterações que estiverem em conflito. Nenhum erro ocorrerá, mas as propriedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> e <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indicarão o número de conflitos e as linhas afetadas por conflitos, respectivamente (somente espaços de trabalho ODBCDirect).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use **Update** para salvar o registro atual e quaisquer alterações feitas nele.

> [!IMPORTANT]
> [!IMPORTANTE] As alterações do registro atual serão perdidas se:
> - Você utilizar os métodos **Edit** ou **AddNew** e mover para outro registro sem primeiro usar **Update**.
> - Você utilizar **Edit** ou **AddNew** e, em seguida, usar **Edit** ou **AddNew** novamente sem primeiro usar **Update**.
> - Você definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** para outro registro.
> - Você fechar o **Recordset** sem usar primeiro **Update**.
> - Você cancelar a operação **Edit** utilizando **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Para editar um registro, use o método **Edit** para copiar o conteúdo do registro atual para um buffer de cópia. Se você não usar **Edit** primeiro, ocorrerá um erro ao usar **Update** ou tentar alterar um valor de campo.

Em um espaço de trabalho ODBCDirect, você pode fazer atualizações em lote, desde que a biblioteca de cursores aceite atualizações em lote, e o **Recordset** tenha sido aberto com a opção de bloqueio de lote otimista.

Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade **LockEdits** do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que o método **Update** seja executado ou a edição seja cancelada. Se a configuração da propriedade **LockEdits** é **False** (bloqueado de forma otimista), o registro é bloqueado e comparado ao registro pré-editado antes de ser atualizado no banco de dados. 

Se o registro foi alterado desde o uso do método **Edit**, a operação **Update** falhará. Os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre utilizam bloqueio otimista. Para continuar a operação **Update** com suas alterações, use o método **Update** novamente. Para reverter para o registro como o outro usuário alterou, atualize o registro atual por meio de movimentação 0.

> [!NOTE]
> [!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro de "Permissão negada" na chamada ao método **AddNew**, **Delete** ou **Edit** em um espaço de trabalho do Microsoft Access ou um erro de "Argumento inválido" ocorrerá na chamada a **Update** em um espaço de trabalho ODBCDirect.

## <a name="example"></a>Exemplo

Este exemplo demonstra o método **Update** em conjunto com o método **Edit**.

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo demonstra o método **Update** em conjunto com o método **AddNew**.

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo usa a propriedade **BatchCollisionCount** e o método **Update** para demonstrar a atualização em lote onde todas as colisões são resolvidas pela imposição da atualização em lote.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

<br/>

Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para a execução deste procedimento.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
