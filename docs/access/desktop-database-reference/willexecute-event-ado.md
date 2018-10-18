---
title: Evento WillExecute (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3cdf4764cca2b40cee62f9d66ea748a4e627a5f
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606840"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="2d3a5-102">Evento WillExecute (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d3a5-102">WillExecute Event (ADO)</span></span>


<span data-ttu-id="2d3a5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d3a5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2d3a5-104">O evento **WillExecute** é chamado um pouco antes da execução de um comando pendente, em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d3a5-105">Syntax</span></span>

<span data-ttu-id="2d3a5-106">WillExecute*Source*, *CursorType*, *LockType*, *Opções*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="2d3a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d3a5-107">Parameters</span></span>

  - <span data-ttu-id="2d3a5-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-108">*Source*</span></span>

  - <span data-ttu-id="2d3a5-109">Uma **sequência de caracteres** que contém um comando SQL ou um nome de procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="2d3a5-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-110">*CursorType*</span></span>

  - <span data-ttu-id="2d3a5-111">Um [CursorTypeEnum](cursortypeenum.md) que contém o tipo de cursor para o **Recordset** que será aberto.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="2d3a5-112">Com esse parâmetro, você pode alterar o cursor para qualquer tipo durante uma operação de [abertura](open-method-ado-recordset.md) do **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2d3a5-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="2d3a5-113">Para qualquer outra operação *CursorType* será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="2d3a5-114">*LockType*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-114">*LockType*</span></span>

  - <span data-ttu-id="2d3a5-115">Um [LockTypeEnum](locktypeenum.md) que contém o tipo de bloqueio para o **Recordset** que será aberto.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="2d3a5-116">Com esse parâmetro, você pode alterar o bloqueio para qualquer tipo, durante a operação **Open** do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="2d3a5-117">Para qualquer outra operação *LockType* será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="2d3a5-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-118">*Options*</span></span>

  - <span data-ttu-id="2d3a5-119">Um valor **Long** que indica as opções que podem ser usadas para executar o comando ou abrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="2d3a5-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-120">*adStatus*</span></span>

  - [<span data-ttu-id="2d3a5-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="2d3a5-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="2d3a5-122">Antes que esse evento retorne, defina esse parâmetro como **adStatusUnwantedEvent**, para evitar notificações subsequentes, ou como **adStatusCancel** para solicitar o cancelamento da operação que gerou esse evento.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="2d3a5-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-123">*pCommand*</span></span>

  - <span data-ttu-id="2d3a5-124">O objeto [Command](command-object-ado.md) ao qual essa notificação de evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="2d3a5-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-125">*pRecordset*</span></span>

  - <span data-ttu-id="2d3a5-126">O objeto [Recordset](recordset-object-ado.md) ao qual essa notificação de evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="2d3a5-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="2d3a5-127">*pConnection*</span></span>

  - <span data-ttu-id="2d3a5-128">O objeto [Connection](connection-object-ado.md) ao qual essa notificação de evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d3a5-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d3a5-129">Remarks</span></span>

<span data-ttu-id="2d3a5-130"><<<<<<< Cabeça um evento **WillExecute** pode ocorrer devido a um **Conexão.** [Executar](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **comando.** [Executar](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), ou **Recordset.** O parâmetro *pConnection* do método [Open](open-method-ado-recordset.md) sempre deve conter uma referência válida a um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="2d3a5-130"><<<<<<< HEAD A **WillExecute** event may occur due to a **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="2d3a5-131">Se o evento for devido à **Connection. Execute**, os parâmetros *pRecordset* e *pCommand* são definidos como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="2d3a5-132">Se o evento for devido ao **Recordset**, o parâmetro *pRecordset* fará referência do objeto **Recordset** e o parâmetro *pCommand* é definido como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="2d3a5-133">Se o evento for devido à **Command. Execute**, o parâmetro *pCommand* fará referência o objeto **Command** e o parâmetro *pRecordset* é definido como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>
<span data-ttu-id="2d3a5-134">=== Um evento **WillExecute** pode ocorrer devido a um **Conexão.** [Executar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **comando.** [Executar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), ou **Recordset.** O parâmetro *pConnection* do método [Open](open-method-ado-recordset.md) sempre deve conter uma referência válida a um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="2d3a5-134">======= A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="2d3a5-135">Se o evento for devido à **Connection. Execute**, os parâmetros *pRecordset* e *pCommand* são definidos como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-135">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="2d3a5-136">Se o evento for devido ao **Recordset**, o parâmetro *pRecordset* fará referência do objeto **Recordset** e o parâmetro *pCommand* é definido como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-136">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="2d3a5-137">Se o evento for devido à **Command. Execute**, o parâmetro *pCommand* fará referência o objeto **Command** e o parâmetro *pRecordset* é definido como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-137">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>
>>>>>>> <span data-ttu-id="2d3a5-138">mestre</span><span class="sxs-lookup"><span data-stu-id="2d3a5-138">master</span></span>

<span data-ttu-id="2d3a5-p104">**WillExecute** permite examinar e modificar os parâmetros de execução pendentes. Esse evento pode retornar uma solicitação para que o comando pendente seja cancelado.</span><span class="sxs-lookup"><span data-stu-id="2d3a5-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

