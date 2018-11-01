---
title: Método Recordset.Update (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48ab6c6c2aa61fbfda52b60c88dfd301742aaf87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891083"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="89b6a-102">Método Recordset.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="89b6a-102">Recordset.Update Method (DAO)</span></span>

<span data-ttu-id="89b6a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="89b6a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="89b6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89b6a-104">Syntax</span></span>

<span data-ttu-id="89b6a-105">*expressão* . Atualização (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="89b6a-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="89b6a-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="89b6a-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="89b6a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89b6a-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b6a-108">Nome</span><span class="sxs-lookup"><span data-stu-id="89b6a-108">Name</span></span></p></th>
<th><p><span data-ttu-id="89b6a-109">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="89b6a-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="89b6a-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="89b6a-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="89b6a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="89b6a-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b6a-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="89b6a-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="89b6a-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="89b6a-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="89b6a-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="89b6a-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="89b6a-115">Uma constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> indicando o tipo de atualização, como especificado em Configurações (somente espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="89b6a-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b6a-116">Force</span><span class="sxs-lookup"><span data-stu-id="89b6a-116">Force</span></span></p></td>
<td><p><span data-ttu-id="89b6a-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="89b6a-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="89b6a-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="89b6a-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="89b6a-p101">Um valor <strong>Boolean</strong> indicando se é preciso impor ou não as alterações ao banco de dados, independentemente de os dados subjacentes terem sido alterados por outro usuário desde a chamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Se for <strong>True</strong>, as alterações serão impostas e as alterações feitas por outros usuários serão simplesmente substituídas. Se for <strong>False</strong> (padrão), as alterações feitas por outro usuário enquanto a atualização estiver pendente causarão uma falha na atualização para as alterações que estiverem em conflito. Nenhum erro ocorrerá, mas as propriedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> e <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indicarão o número de conflitos e as linhas afetadas por conflitos, respectivamente (somente espaços de trabalho ODBCDirect).  </span><span class="sxs-lookup"><span data-stu-id="89b6a-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="89b6a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="89b6a-123">Remarks</span></span>

<span data-ttu-id="89b6a-124">Use **Update** para salvar o registro atual e quaisquer alterações feitas nele.</span><span class="sxs-lookup"><span data-stu-id="89b6a-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89b6a-125">[!IMPORTANTE] As alterações do registro atual serão perdidas se:</span><span class="sxs-lookup"><span data-stu-id="89b6a-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="89b6a-126">Você utilizar os métodos **Edit** ou **AddNew** e mover para outro registro sem primeiro usar **Update**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="89b6a-127">Você utilizar **Edit** ou **AddNew** e, em seguida, usar **Edit** ou **AddNew** novamente sem primeiro usar **Update**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="89b6a-128">Você definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** para outro registro.</span><span class="sxs-lookup"><span data-stu-id="89b6a-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="89b6a-129">Você fechar o **Recordset** sem usar primeiro **Update**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="89b6a-130">Você cancelar a operação **Edit** utilizando **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="89b6a-p102">Para editar um registro, use o método **Edit** para copiar o conteúdo do registro atual para um buffer de cópia. Se você não usar **Edit** primeiro, ocorrerá um erro ao usar **Update** ou tentar alterar um valor de campo.</span><span class="sxs-lookup"><span data-stu-id="89b6a-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="89b6a-133">Em um espaço de trabalho ODBCDirect, você pode fazer atualizações em lote, desde que a biblioteca de cursores aceite atualizações em lote, e o **Recordset** tenha sido aberto com a opção de bloqueio de lote otimista.</span><span class="sxs-lookup"><span data-stu-id="89b6a-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="89b6a-134">Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade **LockEdits** do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que o método **Update** seja executado ou a edição seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="89b6a-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="89b6a-135">Se a configuração da propriedade **LockEdits** é **False** (bloqueado de forma otimista), o registro é bloqueado e comparado ao registro pré-editado antes de ser atualizado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="89b6a-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="89b6a-136">Se o registro foi alterado desde o uso do método **Edit**, a operação **Update** falhará.</span><span class="sxs-lookup"><span data-stu-id="89b6a-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="89b6a-137">Os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre utilizam bloqueio otimista.</span><span class="sxs-lookup"><span data-stu-id="89b6a-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="89b6a-138">Para continuar a operação **Update** com suas alterações, use o método **Update** novamente.</span><span class="sxs-lookup"><span data-stu-id="89b6a-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="89b6a-139">Para reverter para o registro como o outro usuário alterou, atualize o registro atual por meio de movimentação 0.</span><span class="sxs-lookup"><span data-stu-id="89b6a-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="89b6a-p105">[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro de "Permissão negada" na chamada ao método **AddNew**, **Delete** ou **Edit** em um espaço de trabalho do Microsoft Access ou um erro de "Argumento inválido" ocorrerá na chamada a **Update** em um espaço de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="89b6a-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="89b6a-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="89b6a-142">Example</span></span>

<span data-ttu-id="89b6a-143">Este exemplo demonstra o método **Update** em conjunto com o método **Edit**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

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

<span data-ttu-id="89b6a-144">Este exemplo demonstra o método **Update** em conjunto com o método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="89b6a-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

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

<span data-ttu-id="89b6a-145">Este exemplo usa a propriedade **BatchCollisionCount** e o método **Update** para demonstrar a atualização em lote onde todas as colisões são resolvidas pela imposição da atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="89b6a-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

<span data-ttu-id="89b6a-p106">Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="89b6a-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
