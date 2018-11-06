---
title: Propriedade Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfb24f1fd183dd917b1eeb4033fe53a3310d5a12
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997011"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="54983-102">Propriedade Recordset2.LockEdits (DAO)</span><span class="sxs-lookup"><span data-stu-id="54983-102">Recordset2.LockEdits property (DAO)</span></span>

<span data-ttu-id="54983-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="54983-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54983-104">Define ou retorna um valor que indica o tipo de bloqueio ativo durante a edição.</span><span class="sxs-lookup"><span data-stu-id="54983-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="54983-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54983-105">Syntax</span></span>

<span data-ttu-id="54983-106">*expressão* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="54983-106">*expression* .LockEdits</span></span>

<span data-ttu-id="54983-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="54983-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54983-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="54983-108">Remarks</span></span>

<span data-ttu-id="54983-109">O valor de configuração ou de retorno indica o tipo de bloqueio, conforme especificado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="54983-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54983-110">Valor</span><span class="sxs-lookup"><span data-stu-id="54983-110">Value</span></span></p></th>
<th><p><span data-ttu-id="54983-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="54983-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54983-112">True</span><span class="sxs-lookup"><span data-stu-id="54983-112">True</span></span></p></td>
<td><p><span data-ttu-id="54983-p101">Padrão. Bloqueio pessimista ativo. A página que contém o registro que você estiver editando será bloqueada assim que for chamado o método Edit.</span><span class="sxs-lookup"><span data-stu-id="54983-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54983-116">False</span><span class="sxs-lookup"><span data-stu-id="54983-116">False</span></span></p></td>
<td><p><span data-ttu-id="54983-117">Bloqueio otimista está em vigor para edição.</span><span class="sxs-lookup"><span data-stu-id="54983-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="54983-118">A página que contém o registro não está protegida até que o método de atualização é executado.</span><span class="sxs-lookup"><span data-stu-id="54983-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54983-119">Use a propriedade **LockEdits** com os objetos **[Recordset](recordset-object-dao.md)** atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="54983-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="54983-p103">Se uma página estiver bloqueada, nenhum outro usuário poderá editar registros na mesma página. Se você definir **LockEdits** como **True** e outro usuário já tiver bloqueado a página, ocorrerá um erro quando você usar o método **Edit**. Os outros usuários poderão ler os dados das páginas bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="54983-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="54983-p104">Se você definir a propriedade **LockEdits** como **False** e mais tarde usar o método **Update** ao mesmo tempo que outro usuário bloquear a página, ocorrerá um erro. Para ver as alterações feitas no seu registro pelo outro usuário, use o método **[Move](recordset2-move-method-dao.md)** com 0 como argumento; no entanto, se você fizer isso, perderá todas as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="54983-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="54983-p105">Durante o trabalho com o mecanismo do banco de dados do Microsoft Access conectado a fontes de dados ODBC, a propriedade **LockEdits** será definida sempre como **False** ou bloqueio otimista. O mecanismo de dados do Microsoft Access não tem controle sobre os mecanismos de bloqueio usados nos servidores de bancos de dados externos.</span><span class="sxs-lookup"><span data-stu-id="54983-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="54983-127">Você pode predefinir o valor da **LockEdits** quando você primeiro abre o **Recordset** , definindo o argumento lockedits do método **[OpenRecordset](connection-openrecordset-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="54983-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="54983-128">Definir o argumento lockedits como **dbPessimistic** definirá a propriedade **LockEdits** como **True**e lockedits de configuração para qualquer outro valor definirá a propriedade **LockEdits** como **False**.</span><span class="sxs-lookup"><span data-stu-id="54983-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="54983-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="54983-129">Example</span></span>

<span data-ttu-id="54983-p107">Este exemplo demonstra o bloqueio pessimista pela definição da propriedade **LockEdits** como **True** e depois demonstra o bloqueio otimista pela definição da propriedade **LockEdits** como False. Além disso, demonstra qual tipo de tratamento de erros será necessário em um ambiente de banco de dados multiusuário para modificar um campo. As funções PessimisticLock e OptimisticLock são necessárias para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="54983-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
