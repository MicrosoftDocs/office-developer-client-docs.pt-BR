---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282793"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="2bed0-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2bed0-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="2bed0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bed0-105">Dá acesso ao spooler MAPI a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="2bed0-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bed0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2bed0-106">Header file:</span></span>  <br/> |<span data-ttu-id="2bed0-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="2bed0-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2bed0-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="2bed0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2bed0-109">Objetos de logon de transporte</span><span class="sxs-lookup"><span data-stu-id="2bed0-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="2bed0-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2bed0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2bed0-111">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="2bed0-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="2bed0-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2bed0-112">Called by:</span></span>  <br/> |<span data-ttu-id="2bed0-113">O spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="2bed0-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="2bed0-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="2bed0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2bed0-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="2bed0-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="2bed0-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="2bed0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2bed0-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="2bed0-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2bed0-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="2bed0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2bed0-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="2bed0-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="2bed0-120">Retorna os tipos de destinatários que o provedor de transporte manipula.</span><span class="sxs-lookup"><span data-stu-id="2bed0-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="2bed0-121">**Registraroptions**</span><span class="sxs-lookup"><span data-stu-id="2bed0-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="2bed0-122">*Não suportado ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="2bed0-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="2bed0-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="2bed0-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="2bed0-124">Sinaliza a ocorrência de um evento sobre o qual o provedor de transporte solicitou a notificação.</span><span class="sxs-lookup"><span data-stu-id="2bed0-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-125">Estado</span><span class="sxs-lookup"><span data-stu-id="2bed0-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="2bed0-126">Indica que o sistema está ocioso, permitindo que o provedor de transporte realize operações de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="2bed0-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="2bed0-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="2bed0-128">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="2bed0-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="2bed0-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="2bed0-130">Indica que o spooler MAPI tem uma mensagem para o provedor de transporte fornecer.</span><span class="sxs-lookup"><span data-stu-id="2bed0-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-131">Mensagem de email</span><span class="sxs-lookup"><span data-stu-id="2bed0-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="2bed0-132">Informa ao provedor de transporte que o spooler MAPI concluiu seu processamento em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="2bed0-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-133">Quanto</span><span class="sxs-lookup"><span data-stu-id="2bed0-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="2bed0-134">Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="2bed0-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="2bed0-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="2bed0-136">Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bed0-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="2bed0-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="2bed0-138">Abre o objeto status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="2bed0-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="2bed0-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="2bed0-140">Verifica o status externo do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="2bed0-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="2bed0-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2bed0-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="2bed0-142">Solicita que o provedor de transporte entregue imediatamente todas as mensagens pendentes de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="2bed0-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2bed0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bed0-143">See also</span></span>



[<span data-ttu-id="2bed0-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2bed0-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

