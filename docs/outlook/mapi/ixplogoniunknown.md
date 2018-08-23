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
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581402"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="977fc-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="977fc-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="977fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="977fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="977fc-105">Concede o acesso de spooler MAPI para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="977fc-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="977fc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="977fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="977fc-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="977fc-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="977fc-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="977fc-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="977fc-109">Objetos de logon de transporte</span><span class="sxs-lookup"><span data-stu-id="977fc-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="977fc-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="977fc-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="977fc-111">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="977fc-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="977fc-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="977fc-112">Called by:</span></span>  <br/> |<span data-ttu-id="977fc-113">O MAPI spooler</span><span class="sxs-lookup"><span data-stu-id="977fc-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="977fc-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="977fc-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="977fc-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="977fc-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="977fc-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="977fc-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="977fc-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="977fc-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="977fc-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="977fc-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="977fc-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="977fc-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="977fc-120">Retorna os tipos de destinatários que processa o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="977fc-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="977fc-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="977fc-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="977fc-122">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="977fc-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="977fc-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="977fc-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="977fc-124">Sinaliza a ocorrência de um evento sobre quais o provedor de transporte solicitado notificação.</span><span class="sxs-lookup"><span data-stu-id="977fc-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="977fc-125">Ocioso</span><span class="sxs-lookup"><span data-stu-id="977fc-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="977fc-126">Indica que o sistema está ocioso, permitindo que o provedor de transporte executar operações de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="977fc-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="977fc-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="977fc-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="977fc-128">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="977fc-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="977fc-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="977fc-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="977fc-130">Indica que o MAPI spooler tem uma mensagem para o provedor de transporte fornecer.</span><span class="sxs-lookup"><span data-stu-id="977fc-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="977fc-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="977fc-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="977fc-132">Informa o provedor de transporte que o MAPI spooler concluído seu processamento em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="977fc-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="977fc-133">Votação</span><span class="sxs-lookup"><span data-stu-id="977fc-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="977fc-134">Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="977fc-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="977fc-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="977fc-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="977fc-136">Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="977fc-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="977fc-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="977fc-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="977fc-138">Abre o objeto de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="977fc-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="977fc-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="977fc-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="977fc-140">Verifica o status de externo do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="977fc-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="977fc-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="977fc-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="977fc-142">Solicita que o provedor de transporte imediatamente entrega todas as mensagens de entrada ou saídas pendentes.</span><span class="sxs-lookup"><span data-stu-id="977fc-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="977fc-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="977fc-143">See also</span></span>



[<span data-ttu-id="977fc-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="977fc-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

