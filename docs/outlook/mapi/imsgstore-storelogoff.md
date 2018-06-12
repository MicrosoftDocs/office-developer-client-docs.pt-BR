---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767507"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="9af11-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="9af11-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="9af11-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9af11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9af11-105">Habilita o logoff ordenado o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9af11-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9af11-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9af11-106">Parameters</span></span>

 <span data-ttu-id="9af11-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="9af11-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="9af11-108">[além, out] Uma bitmask dos sinalizadores que controla o logoff do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9af11-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="9af11-109">Na entrada, todos os sinalizadores definido para este parâmetro são mutuamente exclusivos; um chamador deve especificar somente um sinalizador por chamada.</span><span class="sxs-lookup"><span data-stu-id="9af11-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="9af11-110">Sinalizadores a seguir são válidos na entrada:</span><span class="sxs-lookup"><span data-stu-id="9af11-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="9af11-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="9af11-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="9af11-112">Qualquer atividade de provedor de transporte para este armazenamento de mensagens deve ser interrompida antes de fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="9af11-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="9af11-113">Controle é retornado para o chamador após a atividade foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="9af11-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="9af11-114">Se qualquer atividade de provedor de transporte está ocorrendo, não ocorrerá o logoff e não ocorrerá nenhuma alteração no comportamento dos provedores de transporte ou spooler de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9af11-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="9af11-115">Se a atividade de provedor de transporte está ociosa, o MAPI spooler libera o repositório.</span><span class="sxs-lookup"><span data-stu-id="9af11-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="9af11-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="9af11-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="9af11-117">O armazenamento de mensagens não deve aguardar para mensagens de provedores de transporte antes de fechar.</span><span class="sxs-lookup"><span data-stu-id="9af11-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="9af11-118">Mensagens de saída que estão prontas para serem enviados são enviadas.</span><span class="sxs-lookup"><span data-stu-id="9af11-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="9af11-119">Se esse repositório contiver a caixa de entrada padrão, todas as mensagens de em processo são recebidas e, em seguida, recepção adicional é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="9af11-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="9af11-120">Quando todas as atividades estiver concluída, o MAPI spooler libera o repositório e controle imediatamente é retornado ao chamador.</span><span class="sxs-lookup"><span data-stu-id="9af11-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="9af11-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="9af11-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="9af11-122">O armazenamento de mensagens não deve aguardar para obter informações de provedores de transporte antes de fechar.</span><span class="sxs-lookup"><span data-stu-id="9af11-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="9af11-123">Mensagens que estão sendo processadas forem concluídas, mas nenhum novas mensagens forem processadas.</span><span class="sxs-lookup"><span data-stu-id="9af11-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="9af11-124">Quando todas as atividades estiver concluída, o MAPI spooler libera o repositório e controle imediatamente é retornado para o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9af11-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="9af11-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="9af11-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="9af11-126">O logoff deve funcionar o mesmo como se o sinalizador LOGOFF_NO_WAIT estiver definido, mas o [IXPLogon::FlushQueues](ixplogon-flushqueues.md) [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) método ou para os provedores de transporte adequado deve ser chamado.</span><span class="sxs-lookup"><span data-stu-id="9af11-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="9af11-127">O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="9af11-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="9af11-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="9af11-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="9af11-129">Se qualquer atividade de provedor de transporte está ocorrendo, o logoff não deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="9af11-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="9af11-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="9af11-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="9af11-131">Mensagens de entrada chegam no momento.</span><span class="sxs-lookup"><span data-stu-id="9af11-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="9af11-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="9af11-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="9af11-133">Mensagens de saída são no processo que está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="9af11-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="9af11-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9af11-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="9af11-135">Mensagens de saída estão pendentes (ou seja, eles são na caixa de saída).</span><span class="sxs-lookup"><span data-stu-id="9af11-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9af11-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9af11-136">Return value</span></span>

<span data-ttu-id="9af11-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9af11-137">S_OK</span></span> 
  
> <span data-ttu-id="9af11-138">O logoff concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="9af11-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9af11-139">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="9af11-139">Remarks</span></span>

<span data-ttu-id="9af11-140">O método **IMsgStore::StoreLogoff** exerce controle sobre a interação da mensagem armazenar e provedores de transporte durante o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="9af11-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="9af11-141">Chamar **StoreLogoff** é válida apenas para repositórios de mensagem que estão sendo usados somente pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9af11-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="9af11-142">Por exemplo, quando dois clientes estão usando o mesmo armazenamento de mensagens e um deles chama **StoreLogoff**, o armazenamento de mensagens é liberado imediatamente e o controle é retornado para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="9af11-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9af11-143">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="9af11-143">Notes to implementers</span></span>

<span data-ttu-id="9af11-144">Salve os sinalizadores que são passados para **StoreLogoff** e passá-las quando você chama o método [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="9af11-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="9af11-145">Não chame **StoreLogoffTransports** até que a contagem de referência da loja mensagem cai para zero.</span><span class="sxs-lookup"><span data-stu-id="9af11-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="9af11-146">Várias chamadas para **StoreLogoffTransports** simplesmente substituem os sinalizadores salvos.</span><span class="sxs-lookup"><span data-stu-id="9af11-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="9af11-147">Se nenhuma chamada foi feita para **StoreLogoff** antes da mensagem contagem de referência da loja chega a zero, defina o sinalizador LOGOFF_ABORT no parâmetro _ulFlags_ que você passa para **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="9af11-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9af11-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="9af11-148">See also</span></span>



[<span data-ttu-id="9af11-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9af11-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="9af11-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="9af11-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="9af11-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9af11-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="9af11-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9af11-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

