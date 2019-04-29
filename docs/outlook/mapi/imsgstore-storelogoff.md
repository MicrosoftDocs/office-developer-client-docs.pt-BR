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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424333"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="2ad2d-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="2ad2d-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="2ad2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ad2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ad2d-105">Permite o logoff ordenada do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2ad2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ad2d-106">Parameters</span></span>

 <span data-ttu-id="2ad2d-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ad2d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="2ad2d-108">[in, out] Uma bitmask de sinalizadores que controla o logoff do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="2ad2d-109">Na entrada, todos os sinalizadores definidos para esse parâmetro são mutuamente exclusivos; um chamador deve especificar apenas um sinalizador por chamada.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="2ad2d-110">Os seguintes sinalizadores são válidos na entrada:</span><span class="sxs-lookup"><span data-stu-id="2ad2d-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="2ad2d-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="2ad2d-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="2ad2d-112">Qualquer atividade do provedor de transporte para esse repositório de mensagens deve ser interrompida antes do logoff.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="2ad2d-113">O controle é retornado ao chamador após a interrupção da atividade.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="2ad2d-114">Se alguma atividade de provedor de transporte estiver ocorrendo, o logoff não ocorrerá e não ocorrerá alteração no comportamento do spooler MAPI ou provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="2ad2d-115">Se a atividade do provedor de transporte estiver ociosa, o spooler MAPI libera o repositório.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="2ad2d-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="2ad2d-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="2ad2d-117">O repositório de mensagens não deve aguardar mensagens de provedores de transporte antes de fechar.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="2ad2d-118">São enviadas mensagens de saída prontas para envio.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="2ad2d-119">Se esse repositório contiver a caixa de entrada padrão, qualquer mensagem em andamento será recebida e, em seguida, a recepção estará desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="2ad2d-120">Quando toda a atividade é concluída, o spooler MAPI libera o repositório e o controle é imediatamente retornado para o chamador.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="2ad2d-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="2ad2d-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="2ad2d-122">O repositório de mensagens não deve aguardar informações de provedores de transporte antes de fechar.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="2ad2d-123">As mensagens que estão sendo processadas atualmente foram concluídas, mas nenhuma mensagem nova é processada.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="2ad2d-124">Quando toda a atividade é concluída, o spooler MAPI libera o repositório e o controle é imediatamente retornado ao provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="2ad2d-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="2ad2d-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="2ad2d-126">O logoff deve funcionar da mesma forma que se o sinalizador LOGOFF_NO_WAIT estiver definido, mas o método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ou [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) para os provedores de transporte apropriados deverá ser chamado.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="2ad2d-127">O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="2ad2d-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="2ad2d-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="2ad2d-129">Se alguma atividade do provedor de transporte estiver ocorrendo, o logoff não deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="2ad2d-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="2ad2d-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="2ad2d-131">As mensagens de entrada estão chegando no momento.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="2ad2d-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="2ad2d-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="2ad2d-133">As mensagens de saída estão no processo de envio.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="2ad2d-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="2ad2d-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="2ad2d-135">As mensagens de saída estão pendentes (ou seja, elas estão na mensagem de saída).</span><span class="sxs-lookup"><span data-stu-id="2ad2d-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ad2d-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ad2d-136">Return value</span></span>

<span data-ttu-id="2ad2d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ad2d-137">S_OK</span></span> 
  
> <span data-ttu-id="2ad2d-138">O logoff foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ad2d-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ad2d-139">Remarks</span></span>

<span data-ttu-id="2ad2d-140">O método **IMsgStore:: StoreLogoff** exerce controle sobre a interação do armazenamento de mensagens e dos provedores de transporte durante o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="2ad2d-141">Chamar **StoreLogoff** é válido somente para repositórios de mensagens que estão sendo usados apenas pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="2ad2d-142">Por exemplo, quando dois clientes estão usando o mesmo repositório de mensagens e um deles chama **StoreLogoff**, o repositório de mensagens é lançado imediatamente e o controle é retornado ao cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2ad2d-143">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="2ad2d-143">Notes to implementers</span></span>

<span data-ttu-id="2ad2d-144">Salve os sinalizadores passados para **StoreLogoff** e passe-os quando chamar o método [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad2d-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="2ad2d-145">Não chame **StoreLogoffTransports** até que a contagem de referência do repositório de mensagens descarte para zero.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="2ad2d-146">Várias chamadas para **StoreLogoffTransports** simplesmente substituem os sinalizadores salvos.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="2ad2d-147">Se nenhuma chamada tiver sido feita ao **StoreLogoff** antes que a contagem de referência do repositório de mensagens atinja zero, defina o sinalizador LOGOFF_ABORT no parâmetro _parâmetroulflags_ que você passa para **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ad2d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ad2d-148">See also</span></span>



[<span data-ttu-id="2ad2d-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2ad2d-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="2ad2d-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="2ad2d-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="2ad2d-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2ad2d-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="2ad2d-152">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2ad2d-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

