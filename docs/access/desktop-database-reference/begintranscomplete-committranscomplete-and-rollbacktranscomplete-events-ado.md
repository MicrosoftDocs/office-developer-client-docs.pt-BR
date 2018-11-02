---
title: Eventos BeginTransComplete, CommitTransComplete, eventos de RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6a49b08c1b4f7879d50f9dd1d29cfcf89ded50c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928073"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="e518c-102">Eventos BeginTransComplete, CommitTransComplete e RollbackTransComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="e518c-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>


<span data-ttu-id="e518c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e518c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e518c-104">Esses eventos serão chamados depois que a operação associada no objeto [Connection](connection-object-ado.md) terminar a execução.</span><span class="sxs-lookup"><span data-stu-id="e518c-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="e518c-105">**BeginTransComplete** é chamado após a operação [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e518c-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="e518c-106">**CommitTransComplete** é chamado após a operação [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e518c-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="e518c-107">**RollbackTransComplete** é chamado após a operação [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e518c-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e518c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e518c-108">Syntax</span></span>

<span data-ttu-id="e518c-109">Do eventos BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="e518c-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="e518c-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="e518c-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="e518c-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="e518c-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="e518c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e518c-112">Parameters</span></span>

  - <span data-ttu-id="e518c-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="e518c-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="e518c-114">Um valor **Long** que contém o novo nível de transação do **BeginTrans** que provocou esse evento.</span><span class="sxs-lookup"><span data-stu-id="e518c-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="e518c-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="e518c-115">*pError*</span></span>

  - <span data-ttu-id="e518c-p101">Um objeto [Error](error-object-ado.md). Ele descreve o erro que ocorreu se o valor EventStatusEnum for **adStatusErrorsOccurred**; caso contrário, ele não está definido.</span><span class="sxs-lookup"><span data-stu-id="e518c-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="e518c-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="e518c-118">*adStatus*</span></span>

  - [<span data-ttu-id="e518c-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="e518c-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="e518c-120">Esses eventos podem impedir notificações subsequentes, definindo esse parâmetro como **adStatusUnwantedEvent** antes que o evento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="e518c-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="e518c-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="e518c-121">*pConnection*</span></span>

  - <span data-ttu-id="e518c-122">O objeto **Connection** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e518c-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e518c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e518c-123">Remarks</span></span>

<span data-ttu-id="e518c-p102">No Visual C++, várias **Conexões** podem compartilhar o mesmo método de tratamento de eventos. O método usa o objeto **Connection** retornado para determinar o objeto que provocou o evento.</span><span class="sxs-lookup"><span data-stu-id="e518c-p102">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="e518c-p103">Se a propriedade [Attributes](attributes-property-ado.md) estiver definida como **adXactCommitRetaining** ou **adXactAbortRetaining**, uma nova transação será iniciada depois de confirmar ou cancelar uma transação. Use o evento **BeginTransComplete** para ignorar tudo, menos o primeiro evento de início de transação.</span><span class="sxs-lookup"><span data-stu-id="e518c-p103">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

