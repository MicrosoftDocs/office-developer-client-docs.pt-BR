---
title: Modo imediato (referência de banco de dados da área de trabalho do Access)
TOCTitle: Immediate Mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 202626b656c79d703d6e06fc4311c9f3bef9fd93
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462355"
---
# <a name="immediate-mode"></a><span data-ttu-id="08885-102">Modo imediato</span><span class="sxs-lookup"><span data-stu-id="08885-102">Immediate Mode</span></span>


<span data-ttu-id="08885-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="08885-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08885-p101">O modo imediato entra em vigor quando a propriedade **LockType** é definida como **adLockOptimistic** ou **adLockPessimistic**. Nesse modo, as alterações feitas em um registro são propagadas na fonte de dados logo que você declara concluído o trabalho em uma linha chamando o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="08885-p101">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**. In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="08885-106">Chamando o método Update</span><span class="sxs-lookup"><span data-stu-id="08885-106">Calling Update</span></span>

<span data-ttu-id="08885-p102">Se você sair do registro que está adicionando ou editando, antes de chamar o método **Update**, o ADO chamará automaticamente o método **Update** para salvar as alterações. Você deverá chamar o método **CancelUpdate** antes da navegação se quiser cancelar as alterações feitas no registro atual ou descartar um registro recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="08885-p102">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="08885-109">O registro atual permanecerá atual após a chamada do método **Update**.</span><span class="sxs-lookup"><span data-stu-id="08885-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="08885-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="08885-110">CancelUpdate</span></span>

<span data-ttu-id="08885-p103">Use o método **CancelUpdate** para cancelar as alterações feitas na linha atual ou descartar uma linha recém-adicionada. Você não pode cancelar as alterações feitas na linha atual ou em uma nova linha após a chamada do método **Update**, a menos que as alterações façam parte de uma transação que você possa cancelar com o método **RollbackTrans** ou parte de uma atualização em lotes. No caso de uma atualização em lotes, é possível cancelar o método **Update** com o método **CancelUpdate** ou **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="08885-p103">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="08885-114">Se você estiver adicionando uma nova linha ao chamar o método **CancelUpdate**, a linha atual se tornará a linha que era atual antes da chamada de **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="08885-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="08885-115">Se você não tiver alterado a linha atual nem adicionado uma nova linha, a chamada do método **CancelUpdate** gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="08885-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

