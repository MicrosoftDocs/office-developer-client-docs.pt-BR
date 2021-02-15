---
title: Exclusão de registros com o método Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293963"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="8f2d8-102">Exclusão de registros com o método Delete</span><span class="sxs-lookup"><span data-stu-id="8f2d8-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="8f2d8-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f2d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f2d8-p101">O uso do método **Delete** marca o registro atual ou um grupo de registros em um objeto **Recordset**, para exclusão. Se o objeto **Recordset** não permitir a exclusão de registros, ocorrerá um erro. Se você estiver no modo de atualização imediata, as exclusões ocorrerão imediatamente no banco de dados. Se um registro não puder ser excluído com êxito (devido a violações de integridade do banco de dados, por exemplo), ele permanecerá no modo de edição após a chamada para **Update**. Isso significa que você deve cancelar a atualização usando [CancelUpdate](cancelupdate-method-ado.md) antes de mover o registro atual (por exemplo, usando [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p101">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion. If the **Recordset** object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="8f2d8-p102">Se você estiver no modo de atualização em lotes, os registros serão marcados para exclusão a partir do cache e a exclusão propriamente dita ocorrerá quando você chamar o método **UpdateBatch**. (Para exibir os registros excluídos, defina a propriedade **Filter** como **adFilterAffectedRecords** após a chamada de **Delete**.)</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p102">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method. (To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="8f2d8-p103">A tentativa de recuperar valores de campo do registro excluído gera um erro. Após a exclusão do registro atual, ele permanecerá atual até você passar para um registro diferente. Quando você se move para longe do registro excluído, ele deixa de ser acessível.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p103">Attempting to retrieve field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="8f2d8-p104">Se você aninhar exclusões em uma transação, poderá recuperar registros excluídos usando o método **RollbackTrans**. Se estiver no modo de atualização em lotes, você poderá cancelar uma exclusão ou um grupo de exclusões pendentes usando o método **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p104">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="8f2d8-p105">Se a tentativa de excluir registros falhar devido a um conflito com os dados subjacentes (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção **Errors**, mas não interromperá a execução do programa. Um erro em tempo de execução só ocorrerá se houver conflitos em todos os registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p105">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="8f2d8-118">Se a propriedade dinâmica **Unique Table** estiver definida e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, o método **Delete** excluirá linhas apenas da tabela nomeada na propriedade **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="8f2d8-p106">O método **Delete** usa um argumento opcional que permite especificar quais registros são afetados pela operação **Delete**. Os únicos valores válidos para esse argumento são uma das seguintes constantes enumeradas **AffectEnum** do ADO:</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p106">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation. The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="8f2d8-121">**adAffectCurrent** Afeta apenas o registro atual.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-121">**adAffectCurrent** Affects only the current record.</span></span>

  - <span data-ttu-id="8f2d8-122">**adAffectGroup** Afeta somente os registros que satisfazem a configuração atual **da propriedade Filter.**</span><span class="sxs-lookup"><span data-stu-id="8f2d8-122">**adAffectGroup** Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="8f2d8-123">A propriedade **Filter** deve ser definida como um valor **FilterGroupEnum** ou uma matriz de **Bookmarks** para usar essa opção.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="8f2d8-p108">O código a seguir mostra um exemplo da especificação de **adAffectGroup** durante a chamada do método **Delete**. Este exemplo adiciona alguns registros ao **Recordset** de exemplo e atualiza o banco de dados. Em seguida, ele filtra o **Recordset** usando a constante enumerada de filtro **adFilterAffectedRecords**, a qual deixa apenas os registro recém-adicionados visíveis no **Recordset**. Finalmente, ele chama o método **Delete** e especifica que todos os registros que satisfazem a configuração atual da propriedade **Filter** (os novos registros) devem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="8f2d8-p108">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method. This example adds some records to the sample **Recordset** and updates the database. Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**. Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

