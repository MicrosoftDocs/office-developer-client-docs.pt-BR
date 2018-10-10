---
title: Método Delete (Recordset do ADO)
TOCTitle: Delete Method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 118cc56bf33812819dd34089ac97c72259228f4c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464350"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="74a68-102">Método Delete (Recordset do ADO)</span><span class="sxs-lookup"><span data-stu-id="74a68-102">Delete Method (ADO Recordset)</span></span>


<span data-ttu-id="74a68-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74a68-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="74a68-104">Exclui o registro atual ou um grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="74a68-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74a68-105">Syntax</span></span>

<span data-ttu-id="74a68-106">*conjunto de registros*. Excluir *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="74a68-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="74a68-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74a68-107">Parameters</span></span>

  - <span data-ttu-id="74a68-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="74a68-108">*AffectRecords*</span></span>

  - <span data-ttu-id="74a68-p101">Um valor [AffectEnum](affectenum.md) que determina quantos registros o método **Delete** afetará. O valor padrão é **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="74a68-p101">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect. The default value is **adAffectCurrent**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="74a68-111">[!OBSERVAçãO] <STRONG>adAffectAll</STRONG> e <STRONG>adAffectAllChapters</STRONG> não são argumentos válidos para <STRONG>Delete</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="74a68-111"><STRONG>adAffectAll</STRONG> and <STRONG>adAffectAllChapters</STRONG> are not valid arguments to <STRONG>Delete</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="74a68-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="74a68-112">Remarks</span></span>

<span data-ttu-id="74a68-p102">A utilização do método **Delete** marca o registro atual ou um grupo de registros em um objeto [Recordset](recordset-object-ado.md) para exclusão. Se o objeto **Recordset** não permitir a exclusão de registros, ocorrerá um erro. Se você estiver no modo de atualização imediata, as exclusões ocorrem imediatamente no banco de dados. Se um registro não puder ser excluído com êxito (devido a violações de integridade do banco de dados, por exemplo), o registro permanecerá no modo de edição após a chamada a **Update**. Isso significa que você deve cancelar a atualização com [CancelUpdate](cancelupdate-method-ado.md) antes de mover para fora do registro atual (por exemplo, com [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="74a68-p102">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion. If the **Recordset** object doesn't allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="74a68-p103">Se você estiver no modo de atualização em lote, os registros são marcados para exclusão no cache e a exclusão real ocorrerá quando você chamar o método [UpdateBatch](updatebatch-method-ado.md). (Utilize a propriedade [Filter](filter-property-ado.md) para ver os registros excluídos.)</span><span class="sxs-lookup"><span data-stu-id="74a68-p103">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method. (Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="74a68-p104">A recuperação de valores de campo do registro excluído gera um erro. Depois de excluir o registro atual, o registro excluído permanecerá atual até que você mova para um registro diferente. Depois de mover para fora do registro excluído, ele não mais será acessível.</span><span class="sxs-lookup"><span data-stu-id="74a68-p104">Retrieving field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="74a68-p105">Se você aninhar exclusões em uma transação, é possível recuperar registros excluídos com o método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se você estiver no modo de atualização em lote, poderá cancelar uma exclusão pendente ou um grupo de exclusões pendentes com o método [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="74a68-p105">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="74a68-p106">Se a tentativa de excluir registros falhar devido a um conflito com os dados subjacentes (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção [Errors](errors-collection-ado.md), mas não interromperá a execução do programa. Um erro em tempo de execução só ocorrerá se houver conflitos em todos os registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="74a68-p106">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="74a68-127">Se a propriedade dinâmica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) estiver definida e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, o método **Delete** excluirá linhas apenas da tabela nomeada na propriedade [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="74a68-127">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

