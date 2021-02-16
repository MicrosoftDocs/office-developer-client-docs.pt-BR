---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421379"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="d96d2-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="d96d2-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="d96d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d96d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d96d2-105">Solicita a liberação pedido de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d96d2-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d96d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d96d2-106">Parameters</span></span>

 <span data-ttu-id="d96d2-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d96d2-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d96d2-108">[in, out] Uma máscara de bits de sinalizadores que controla como ocorre o logoff do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d96d2-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="d96d2-109">Na entrada, todos os sinalizadores para esse parâmetro são mutuamente exclusivos; apenas um dos sinalizadores a seguir pode ser definido por chamada:</span><span class="sxs-lookup"><span data-stu-id="d96d2-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="d96d2-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="d96d2-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="d96d2-111">Qualquer atividade do provedor de transporte para este armazenamento deve ser interrompida antes de fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="d96d2-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="d96d2-112">O controle é retornado ao cliente depois que a atividade é interrompida e o spooler MAPI saiu do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d96d2-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="d96d2-113">Se qualquer atividade de transporte estiver ocorrendo, o logoff não ocorrerá e nenhuma alteração no spooler MAPI ou no comportamento do provedor de transporte ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="d96d2-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="d96d2-114">Se não houver nenhuma atividade no momento, o spooler MAPI liberará o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d96d2-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="d96d2-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="d96d2-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="d96d2-116">O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente após o envio de todos os emails de saída que estão prontos para serem enviados.</span><span class="sxs-lookup"><span data-stu-id="d96d2-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="d96d2-117">Se o armazenamento de mensagens tiver a Caixa de Entrada padrão, qualquer mensagem no processo será recebida e, em seguida, a recepção posterior será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d96d2-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="d96d2-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="d96d2-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="d96d2-119">O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente depois que qualquer mensagem pendente terminar o processamento.</span><span class="sxs-lookup"><span data-stu-id="d96d2-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="d96d2-120">Nenhuma mensagem nova deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="d96d2-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="d96d2-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="d96d2-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="d96d2-122">Funciona da mesma forma que o LOGOFF_NO_WAIT sinalizador.</span><span class="sxs-lookup"><span data-stu-id="d96d2-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="d96d2-123">O LOGOFF_PURGE sinalizador retorna o controle ao chamador após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="d96d2-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="d96d2-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="d96d2-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="d96d2-125">O logoff não deve ocorrer se qualquer atividade do provedor de transporte estiver ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="d96d2-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="d96d2-126">O tipo de atividade que está ocorrendo é retornado como um sinalizador na saída.</span><span class="sxs-lookup"><span data-stu-id="d96d2-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="d96d2-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="d96d2-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="d96d2-128">O logoff pode ser concluído.</span><span class="sxs-lookup"><span data-stu-id="d96d2-128">The logoff can complete.</span></span> <span data-ttu-id="d96d2-129">Todos os recursos associados ao armazenamento foram liberados e o objeto foi invalidado.</span><span class="sxs-lookup"><span data-stu-id="d96d2-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="d96d2-130">O spooler MAPI realizou ou executará todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="d96d2-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="d96d2-131">Somente o método **IUnknown::Release** do armazenamento de mensagens deve ser chamado neste ponto.</span><span class="sxs-lookup"><span data-stu-id="d96d2-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="d96d2-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="d96d2-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="d96d2-133">No momento, uma mensagem está chegando à loja de um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="d96d2-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="d96d2-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="d96d2-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="d96d2-135">No momento, uma mensagem está sendo enviada da loja por um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="d96d2-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="d96d2-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="d96d2-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="d96d2-137">Atualmente, há mensagens na fila de saída para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d96d2-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d96d2-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d96d2-138">Return value</span></span>

<span data-ttu-id="d96d2-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="d96d2-139">S_OK</span></span> 
  
> <span data-ttu-id="d96d2-140">O procedimento de logoff foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d96d2-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d96d2-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="d96d2-141">Remarks</span></span>

<span data-ttu-id="d96d2-142">O **método IMAPISupport::StoreLogoffTransports** é implementado para objetos de suporte do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d96d2-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="d96d2-143">Os provedores de armazenamento de mensagens chamam **StoreLogoffTransports** para dar aos aplicativos cliente algum controle sobre como o MAPI lida com a atividade do provedor de transporte à medida que um armazenamento de mensagens está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="d96d2-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="d96d2-144">Se outro processo faz com que o armazenamento seja desconectado para o mesmo perfil, MAPI ignora uma chamada para **StoreLogoffTransports** e retorna o LOGOFF_COMPLETE sinalizador no parâmetro _lpulFlags._</span><span class="sxs-lookup"><span data-stu-id="d96d2-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="d96d2-145">O comportamento do provedor de armazenamento após o retorno de **StoreLogoffTransports** deve ser baseado no valor de  _lpulFlags_, que indica o status do sistema e transmite instruções do cliente para o comportamento de logoff.</span><span class="sxs-lookup"><span data-stu-id="d96d2-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d96d2-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d96d2-146">Notes to callers</span></span>

 <span data-ttu-id="d96d2-147">**StoreLogoffTransports** normalmente é chamado a partir do método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) de um provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="d96d2-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="d96d2-148">No entanto, ele também pode ser chamado a partir do **método IUnknown::Release** do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d96d2-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="d96d2-149">Implemente **o método Release** do seu armazenamento de mensagens para que você possa verificar se ocorreu ou não uma chamada para **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="d96d2-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="d96d2-150">Se não tiver ocorrido uma chamada, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido.</span><span class="sxs-lookup"><span data-stu-id="d96d2-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="d96d2-151">O  _parâmetro lpulFlags_ é definido como um sinalizador que indica como o cliente exige que o armazenamento de mensagens seja desligado.</span><span class="sxs-lookup"><span data-stu-id="d96d2-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="d96d2-152">Determine a configuração apropriada para  _ulFlags_ com base na configuração do parâmetro correspondente na chamada para **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="d96d2-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="d96d2-153">Ou seja, se um cliente chamado seu método **StoreLogoff** com  _ulFlags_ definido como LOGOFF_ORDERLY, você deve chamar **StoreLogoffTransports** com  _ulFlags_ definido como LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="d96d2-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="d96d2-154">Para obter mais informações sobre o processo de logoff do armazenamento de mensagens, consulte [Desligar um Provedor de Armazenamento de Mensagens.](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d96d2-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d96d2-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="d96d2-155">See also</span></span>



[<span data-ttu-id="d96d2-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="d96d2-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="d96d2-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d96d2-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="d96d2-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d96d2-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

