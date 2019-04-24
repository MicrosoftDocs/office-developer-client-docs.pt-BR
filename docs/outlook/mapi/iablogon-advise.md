---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338574"
---
# <a name="iablogonadvise"></a><span data-ttu-id="82c85-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="82c85-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="82c85-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82c85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82c85-105">Registra o chamador para receber notificações de eventos específicos que afetam um contêiner, usuário de mensagens ou lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="82c85-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="82c85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c85-106">Parameters</span></span>

 <span data-ttu-id="82c85-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="82c85-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="82c85-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="82c85-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="82c85-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="82c85-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="82c85-110">no Um ponteiro para o identificador de entrada do objeto sobre quais notificações devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="82c85-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="82c85-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="82c85-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="82c85-112">no Uma máscara de valores que indica os tipos de eventos de notificação nos quais o chamador está interessado e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="82c85-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="82c85-113">Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="82c85-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="82c85-114">A tabela a seguir lista os valores válidos para o parâmetro _ulEventMask_ e as estruturas associadas a cada valor.</span><span class="sxs-lookup"><span data-stu-id="82c85-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="82c85-115">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="82c85-115">**Notification event type**</span></span>|<span data-ttu-id="82c85-116">**Estrutura de **notificação** correspondente**</span><span class="sxs-lookup"><span data-stu-id="82c85-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82c85-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="82c85-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="82c85-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="82c85-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="82c85-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="82c85-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="82c85-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="82c85-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="82c85-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="82c85-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="82c85-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="82c85-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="82c85-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="82c85-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="82c85-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="82c85-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="82c85-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="82c85-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="82c85-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="82c85-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="82c85-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="82c85-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="82c85-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="82c85-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="82c85-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="82c85-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="82c85-130">no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="82c85-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="82c85-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="82c85-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="82c85-132">bota Um ponteiro para um valor diferente de zero que representa o registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="82c85-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82c85-133">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="82c85-133">Return value</span></span>

<span data-ttu-id="82c85-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="82c85-134">S_OK</span></span> 
  
> <span data-ttu-id="82c85-135">O registro de notificação foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="82c85-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="82c85-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82c85-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="82c85-137">O identificador de entrada passado no parâmetro _lpEntryID_ não está no formato apropriado.</span><span class="sxs-lookup"><span data-stu-id="82c85-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="82c85-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="82c85-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="82c85-139">O provedor de catálogo de endereços não oferece suporte a notificações, possivelmente porque não permite que as alterações sejam feitas em seus objetos.</span><span class="sxs-lookup"><span data-stu-id="82c85-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="82c85-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82c85-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="82c85-141">O provedor de catálogo de endereços não pode lidar com o identificador de entrada passado no _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="82c85-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82c85-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c85-142">Remarks</span></span>

<span data-ttu-id="82c85-143">Os provedores de catálogo de endereços implementam o método **IABLogon:: Advise** para registrar o chamador para ser notificado quando uma alteração ocorre para um objeto em um de seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="82c85-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="82c85-144">Os chamadores podem se registrar para obter notificações sobre usuários de mensagens, listas de distribuição ou contêineres inteiros.</span><span class="sxs-lookup"><span data-stu-id="82c85-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="82c85-145">Normalmente, os clientes chamam o método [IAddrBook:: Advise](iaddrbook-advise.md) para registrar notificações do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="82c85-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="82c85-146">Em seguida, o MAPI chama o método **Advise** do provedor de catálogo de endereços responsável pelo objeto representado pelo identificador de entrada no _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="82c85-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="82c85-147">Quando uma alteração ocorre para o objeto indicado do tipo representado no _ulEventMask_, uma chamada é feita ao método OnNotify do coletor de avisos apontado por _lpAdviseSink_. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="82c85-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="82c85-148">Dados passados na estrutura de **notificação** para a \*\*\*\* rotina OnNotify descreve o evento.</span><span class="sxs-lookup"><span data-stu-id="82c85-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="82c85-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="82c85-149">Notes to implementers</span></span>

<span data-ttu-id="82c85-150">Você pode dar suporte à notificação com ou sem a ajuda do MAPI.</span><span class="sxs-lookup"><span data-stu-id="82c85-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="82c85-151">O MAPI tem três métodos de objeto de suporte para ajudar os provedores de serviços a implementar a notificação:</span><span class="sxs-lookup"><span data-stu-id="82c85-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="82c85-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="82c85-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="82c85-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="82c85-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="82c85-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="82c85-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="82c85-155">Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando seu método **Advise** for chamado e libere o ponteiro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="82c85-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="82c85-156">Se você optar por dar suporte a uma notificação por conta própria, chame o método **AddRef** do coletor de avisos representado pelo parâmetro _lpAdviseSink_ para manter uma cópia desse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82c85-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="82c85-157">Mantenha essa cópia até que o método [IABLogon:: Unadvise](iablogon-unadvise.md) seja chamado para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="82c85-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="82c85-158">Independentemente de como você dá suporte à notificação, atribua um número de conexão diferente de zero para o registro de notificação e devolva-o no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="82c85-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="82c85-159">Não libere esse número de conexão até que o método **Unadvise** tenha sido chamado.</span><span class="sxs-lookup"><span data-stu-id="82c85-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82c85-160">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="82c85-160">Notes to callers</span></span>

<span data-ttu-id="82c85-161">O ponteiro de coletor de aviso que você passa no parâmetro _lpAdviseSink_ para **avisar** pode apontar para um objeto que você criou ou que o MAPI criou através da função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="82c85-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="82c85-162">Você pode querer usar **HrThisThreadAdviseSink** se você dá suporte a vários threads de execução e quer ter certeza de que as chamadas subsequentes para seu método OnNotify ocorram em um momento apropriado em um thread apropriado. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="82c85-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="82c85-163">Prepare-se para o seu objeto de coletor de aviso a ser liberado a qualquer momento após a chamada para **avisar** e antes da chamada para **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="82c85-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="82c85-164">Portanto, você deve liberar seu objeto de coletor de \*\*\*\* aviso após a revisor, a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="82c85-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="82c85-165">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="82c85-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="82c85-166">Para obter informações sobre como usar os métodos **IMAPISupport** para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="82c85-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="82c85-167">Para obter mais informações sobre multithreading e MAPI, consulte [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="82c85-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82c85-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="82c85-168">See also</span></span>



[<span data-ttu-id="82c85-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="82c85-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="82c85-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="82c85-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="82c85-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="82c85-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="82c85-172">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="82c85-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="82c85-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82c85-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

