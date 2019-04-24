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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326492"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="ce9ce-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="ce9ce-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="ce9ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce9ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce9ce-105">Solicita o lançamento ordenada de um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ce9ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce9ce-106">Parameters</span></span>

 <span data-ttu-id="ce9ce-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce9ce-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="ce9ce-108">[in, out] Uma bitmask de sinalizadores que controlam como o logoff do repositório de mensagens ocorre.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="ce9ce-109">Na entrada, todos os sinalizadores desse parâmetro são mutuamente exclusivos; apenas um dos seguintes sinalizadores pode ser definido por chamada:</span><span class="sxs-lookup"><span data-stu-id="ce9ce-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="ce9ce-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="ce9ce-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="ce9ce-111">Qualquer atividade do provedor de transporte para este repositório deve ser interrompida antes do logoff.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="ce9ce-112">O controle é retornado ao cliente após a atividade ser interrompida e o spooler MAPI desconectado do repositório.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="ce9ce-113">Se alguma atividade de transporte estiver ocorrendo, o logoff não ocorrerá e não ocorrerá nenhuma alteração no comportamento do spooler MAPI ou do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="ce9ce-114">Se não houver atividade no momento, o spooler MAPI libera o repositório.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="ce9ce-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="ce9ce-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="ce9ce-116">O spooler MAPI deve liberar a loja e retornar o controle para o cliente imediatamente após todos os emails de saída que estão prontos para serem enviados são enviados.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="ce9ce-117">Se o repositório de mensagens tiver a caixa de entrada padrão, qualquer mensagem em andamento será recebida e, em seguida, a recepção será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="ce9ce-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="ce9ce-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="ce9ce-119">O spooler MAPI deve liberar o armazenamento e retornar o controle para o cliente imediatamente após a conclusão do processamento de qualquer mensagem pendente.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="ce9ce-120">Nenhuma mensagem nova deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="ce9ce-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="ce9ce-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="ce9ce-122">Funciona da mesma maneira que o sinalizador LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="ce9ce-123">O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="ce9ce-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="ce9ce-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="ce9ce-125">O logoff não deve ocorrer se qualquer atividade do provedor de transporte estiver ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="ce9ce-126">O tipo de atividade que está sendo realizada é retornado como um sinalizador na saída.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="ce9ce-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ce9ce-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="ce9ce-128">O logoff pode ser concluído.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-128">The logoff can complete.</span></span> <span data-ttu-id="ce9ce-129">Todos os recursos associados ao repositório foram liberados e o objeto foi invalidado.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="ce9ce-130">O spooler MAPI executou ou executará todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="ce9ce-131">Somente o método **IUnknown:: Release** do repositório de mensagens deve ser chamado neste ponto.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="ce9ce-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="ce9ce-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="ce9ce-133">No momento, uma mensagem está chegando ao repositório de um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="ce9ce-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="ce9ce-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="ce9ce-135">No momento, uma mensagem está sendo enviada da loja por um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="ce9ce-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="ce9ce-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="ce9ce-137">Há mensagens no momento na fila de saída para o repositório.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce9ce-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce9ce-138">Return value</span></span>

<span data-ttu-id="ce9ce-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce9ce-139">S_OK</span></span> 
  
> <span data-ttu-id="ce9ce-140">O procedimento de logoff foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce9ce-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce9ce-141">Remarks</span></span>

<span data-ttu-id="ce9ce-142">O método **IMAPISupport:: StoreLogoffTransports** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ce9ce-143">Os provedores de repositório de mensagens chamam o **StoreLogoffTransports** para fornecer aos aplicativos cliente controle sobre como o MAPI lida com a atividade do provedor de transporte, pois um repositório de mensagens está fechando.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="ce9ce-144">Se outro processo tiver o repositório a ser conectado aberto para o mesmo perfil, o MAPI ignorará uma chamada para **StoreLogoffTransports** e retornará o sinalizador LOGOFF_COMPLETE no parâmetro _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ce9ce-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ce9ce-145">O comportamento do provedor de repositório após o retorno de **StoreLogoffTransports** deve se basear no valor de _lpulFlags_, que indica o status do sistema e transmite instruções do cliente para o comportamento de logoff.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce9ce-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ce9ce-146">Notes to callers</span></span>

 <span data-ttu-id="ce9ce-147">**StoreLogoffTransports** normalmente é chamado de um método [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) do provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="ce9ce-148">No enTanto, ele também pode ser chamado a partir do método **IUnknown:: Release** do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="ce9ce-149">Implemente o método **Release** do seu repositório de mensagens para que você possa verificar se uma chamada para **StoreLogoffTransports** ocorreu ou não.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="ce9ce-150">Se uma chamada não tiver ocorrido, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="ce9ce-151">O parâmetro _lpulFlags_ é definido como um sinalizador que indica como o cliente exige que o repositório de mensagens seja desligado.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="ce9ce-152">Determine a configuração apropriada para o _parâmetroulflags_ com base na configuração do parâmetro correspondente na chamada para **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="ce9ce-153">Ou seja, se um cliente chamou o método **StoreLogoff** com _PARÂMETROULFLAGS_ definido como LOGOFF_ORDERLY, você deve chamar **STORELOGOFFTRANSPORTS** com _parâmetroulflags_ definido como LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="ce9ce-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="ce9ce-154">Para obter mais informações sobre o processo de logoff do repositório de mensagens, consulte desLigando [um provedor de armazenamento de mensagens](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce9ce-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce9ce-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce9ce-155">See also</span></span>



[<span data-ttu-id="ce9ce-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="ce9ce-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="ce9ce-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="ce9ce-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="ce9ce-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce9ce-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

