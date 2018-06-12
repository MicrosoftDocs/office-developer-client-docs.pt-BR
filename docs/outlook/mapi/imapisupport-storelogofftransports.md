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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767308"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="86f18-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="86f18-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="86f18-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86f18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86f18-105">Solicita a versão ordenada de um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86f18-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="86f18-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="86f18-106">Parameters</span></span>

 <span data-ttu-id="86f18-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="86f18-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="86f18-108">[além, out] Uma bitmask dos sinalizadores que controla como o logoff do repositório de mensagem ocorre.</span><span class="sxs-lookup"><span data-stu-id="86f18-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="86f18-109">Na entrada, todos os sinalizadores para este parâmetro são mutuamente exclusivos; somente um dos sinalizadores a seguir pode ser definido por chamada:</span><span class="sxs-lookup"><span data-stu-id="86f18-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="86f18-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="86f18-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="86f18-111">Qualquer atividade de provedor de transporte para esse repositório deve ser interrompida antes de fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="86f18-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="86f18-112">Controle é retornado ao cliente após a atividade foi interrompida e o MAPI spooler tiverem feito logoff o repositório.</span><span class="sxs-lookup"><span data-stu-id="86f18-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="86f18-113">Se qualquer atividade de transporte estiver ocorrendo, não ocorrerá o logoff e não ocorrerá nenhuma alteração no comportamento de provedor de transporte ou spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="86f18-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="86f18-114">Se não há atualmente nenhuma atividade, o MAPI spooler libera o repositório.</span><span class="sxs-lookup"><span data-stu-id="86f18-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="86f18-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="86f18-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="86f18-116">O MAPI spooler deve liberar o repositório e retornar o controle para o cliente imediatamente saída depois que todos os emails que está pronta para ser enviada é enviada.</span><span class="sxs-lookup"><span data-stu-id="86f18-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="86f18-117">Se o armazenamento de mensagens tiver a caixa de entrada padrão, qualquer mensagem em processo é recebida e, em seguida, recepção adicional é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="86f18-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="86f18-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="86f18-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="86f18-119">O MAPI spooler deve liberar o repositório e retornar o controle para o cliente imediatamente após pendentes mensagens estiverem terminadas processamento.</span><span class="sxs-lookup"><span data-stu-id="86f18-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="86f18-120">Não há novas mensagens devem ser processadas.</span><span class="sxs-lookup"><span data-stu-id="86f18-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="86f18-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="86f18-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="86f18-122">Funciona da mesma maneira como o sinalizador LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="86f18-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="86f18-123">O sinalizador LOGOFF_PURGE retorna o controle para o chamador após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="86f18-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="86f18-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="86f18-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="86f18-125">O logoff não deve ocorrer se qualquer atividade de provedor de transporte estiver ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="86f18-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="86f18-126">O tipo de atividade ocorrendo é retornado como um sinalizador na saída.</span><span class="sxs-lookup"><span data-stu-id="86f18-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="86f18-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="86f18-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="86f18-128">O logoff pode concluir.</span><span class="sxs-lookup"><span data-stu-id="86f18-128">The logoff can complete.</span></span> <span data-ttu-id="86f18-129">Todos os recursos associados ao repositório foram liberados e o objeto foi invalidado.</span><span class="sxs-lookup"><span data-stu-id="86f18-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="86f18-130">O MAPI spooler realizou ou irá realizar todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="86f18-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="86f18-131">Apenas o método de **IUnknown:: Release** da loja mensagem deve ser chamado neste momento.</span><span class="sxs-lookup"><span data-stu-id="86f18-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="86f18-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="86f18-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="86f18-133">Uma mensagem atualmente vem para o repositório de um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="86f18-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="86f18-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="86f18-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="86f18-135">Uma mensagem atualmente está sendo enviada do repositório por um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="86f18-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="86f18-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="86f18-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="86f18-137">Atualmente existem mensagens na fila de saída para o repositório.</span><span class="sxs-lookup"><span data-stu-id="86f18-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86f18-138">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="86f18-138">Return value</span></span>

<span data-ttu-id="86f18-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="86f18-139">S_OK</span></span> 
  
> <span data-ttu-id="86f18-140">O procedimento de logoff foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="86f18-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86f18-141">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="86f18-141">Remarks</span></span>

<span data-ttu-id="86f18-142">O método **IMAPISupport::StoreLogoffTransports** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86f18-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="86f18-143">Provedores de armazenamento de mensagem chamarem **StoreLogoffTransports** para fornecer aplicativos cliente algum controle sobre como a atividade de provedor de transporte MAPI alças como um armazenamento de mensagens está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="86f18-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="86f18-144">Se outro processo tiver o repositório a ser desconectado de abrir para o mesmo perfil, MAPI ignora uma chamada para **StoreLogoffTransports** e retorna o sinalizador LOGOFF_COMPLETE no parâmetro _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="86f18-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="86f18-145">O comportamento do provedor de repositório seguindo o retorno do **StoreLogoffTransports** deve ter como base o valor da _lpulFlags_, que indica o status do sistema e transmite instruções de cliente para o comportamento de logoff.</span><span class="sxs-lookup"><span data-stu-id="86f18-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="86f18-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="86f18-146">Notes to callers</span></span>

 <span data-ttu-id="86f18-147">**StoreLogoffTransports** geralmente é chamado pelo método de [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) um repositório do provedor.</span><span class="sxs-lookup"><span data-stu-id="86f18-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="86f18-148">No entanto, ele também pode ser chamado pelo método **IUnknown:: Release** o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="86f18-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="86f18-149">Implementar o método de **lançamento** do seu armazenamento de mensagens de modo que você possa verificar se ou não uma chamada para **StoreLogoffTransports** ocorreu.</span><span class="sxs-lookup"><span data-stu-id="86f18-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="86f18-150">Se uma chamada não tiver ocorrido, chame **StoreLogoffTransports** com o sinalizador LOGOFF_ABORT definido.</span><span class="sxs-lookup"><span data-stu-id="86f18-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="86f18-151">O parâmetro _lpulFlags_ é definido como um sinalizador que indica como o cliente requer o armazenamento de mensagens seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="86f18-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="86f18-152">Determine a configuração apropriada para _ulFlags_ com base na configuração do parâmetro correspondente na chamada a **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="86f18-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="86f18-153">Ou seja, se um cliente chamado o método **StoreLogoff** com _ulFlags_ definido como LOGOFF_ORDERLY, você deve chamar **StoreLogoffTransports** com _ulFlags_ definido como LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="86f18-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="86f18-154">Para obter mais informações sobre o processo de logoff do repositório de mensagem, consulte [Sendo para baixo uma mensagem Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="86f18-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86f18-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="86f18-155">See also</span></span>



[<span data-ttu-id="86f18-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="86f18-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="86f18-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="86f18-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="86f18-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="86f18-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

