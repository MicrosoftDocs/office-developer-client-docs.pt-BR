---
title: Método CancelUpdate (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d5414f6f604392d64baba7e67c8b66d13afc94d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922584"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="9b1a2-102">Método CancelUpdate (ADO)</span><span class="sxs-lookup"><span data-stu-id="9b1a2-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="9b1a2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b1a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b1a2-104">Cancela qualquer alteração feita na linha atual ou na nova linha de um objeto [Recordset](recordset-object-ado.md), ou na coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), antes da chamada do método [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b1a2-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b1a2-105">Syntax</span></span>

<span data-ttu-id="9b1a2-106">*conjunto de registros*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="9b1a2-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="9b1a2-107">*registro*. *Campos*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="9b1a2-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="9b1a2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b1a2-108">Remarks</span></span>

<span data-ttu-id="9b1a2-109">**Objeto Recordset**</span><span class="sxs-lookup"><span data-stu-id="9b1a2-109">**Recordset**</span></span>

<span data-ttu-id="9b1a2-p101">Use o método **CancelUpdate** para cancelar as alterações feitas na linha atual ou descartar uma linha recém-adicionada. Você não poderá cancelar as alterações feitas na linha atual ou em uma nova linha após chamar o método **Update**, a menos que as alterações façam parte de uma transação que possa ser revertida com o método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) ou façam parte de uma atualização em lotes. No caso de uma atualização em lotes, você poderá cancelar **Update** com o método **CancelUpdate** ou [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b1a2-p101">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="9b1a2-113">Se, ao chamar o método **CancelUpdate**, você estiver adicionando uma nova linha, a linha atual passará a ser a linha que estava atual antes da chamada de [AddNew](addnew-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b1a2-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="9b1a2-p102">Se estiver no modo de edição e desejar sair do registro atual (por exemplo, com [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md)), você poderá usar **CancelUpdate** para cancelar as alterações pendentes. Esse procedimento será necessário se a atualização não puder ser postada com êxito na fontes de dados (por exemplo, a falha de uma tentativa de exclusão devido a violações de integridade referencial manterá o **Recordset** no modo de edição depois que [Delete](delete-method-ado-recordset.md) for chamado).</span><span class="sxs-lookup"><span data-stu-id="9b1a2-p102">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes. You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="9b1a2-116">**Objeto Record**</span><span class="sxs-lookup"><span data-stu-id="9b1a2-116">**Record**</span></span>

<span data-ttu-id="9b1a2-p103">O método **CancelUpdate** cancela qualquer inserção ou exclusão pendente de objetos [Field](field-object-ado.md), e também cancela as atualizações pendentes de campos existentes, restaurando-os aos seus valores originais. A propriedade [Status](status-property-ado-recordset.md) de todos os campos na coleção **Fields** é definida como **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="9b1a2-p103">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values. The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

