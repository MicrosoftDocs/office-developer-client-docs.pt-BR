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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766847"
---
# <a name="iablogonadvise"></a><span data-ttu-id="4ba64-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4ba64-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="4ba64-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ba64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ba64-105">Registra o chamador para receber notificações de eventos especificados que afetam um contêiner, o usuário ou lista de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4ba64-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4ba64-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4ba64-106">Parameters</span></span>

 <span data-ttu-id="4ba64-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ba64-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4ba64-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4ba64-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4ba64-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ba64-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4ba64-110">[in] Um ponteiro para o identificador de entrada do objeto notificações sobre quais devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="4ba64-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="4ba64-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4ba64-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="4ba64-112">[in] Uma bitmask dos valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="4ba64-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="4ba64-113">Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="4ba64-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="4ba64-114">A tabela a seguir lista os valores válidos para o parâmetro _ulEventMask_ e as estruturas associadas a cada valor.</span><span class="sxs-lookup"><span data-stu-id="4ba64-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="4ba64-115">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="4ba64-115">**Notification event type**</span></span>|<span data-ttu-id="4ba64-116">**Estrutura de **notificação** correspondente**</span><span class="sxs-lookup"><span data-stu-id="4ba64-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ba64-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="4ba64-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="4ba64-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4ba64-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4ba64-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="4ba64-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="4ba64-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4ba64-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4ba64-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="4ba64-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="4ba64-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="4ba64-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="4ba64-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="4ba64-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="4ba64-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="4ba64-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="4ba64-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="4ba64-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="4ba64-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="4ba64-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="4ba64-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="4ba64-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="4ba64-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="4ba64-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="4ba64-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4ba64-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4ba64-130">[in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4ba64-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="4ba64-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4ba64-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="4ba64-132">[out] Um ponteiro para um valor diferente de zero que representa o registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba64-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ba64-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4ba64-133">Return value</span></span>

<span data-ttu-id="4ba64-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ba64-134">S_OK</span></span> 
  
> <span data-ttu-id="4ba64-135">O registro de notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4ba64-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="4ba64-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4ba64-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="4ba64-137">O identificador de entrada passado no parâmetro _lpEntryID_ não está no formato apropriado.</span><span class="sxs-lookup"><span data-stu-id="4ba64-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="4ba64-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4ba64-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4ba64-139">O provedor de catálogo de endereços não suporta notificação, possivelmente porque não permitem que as alterações sejam feitas para seus objetos.</span><span class="sxs-lookup"><span data-stu-id="4ba64-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="4ba64-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4ba64-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4ba64-141">O provedor de catálogo de endereços não pode manipular o identificador de entrada passado _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="4ba64-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ba64-142">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4ba64-142">Remarks</span></span>

<span data-ttu-id="4ba64-143">Provedores de catálogo de endereços implementam o método **IABLogon::Advise** para registrar o chamador para ser notificado quando ocorre uma alteração a um objeto em um dos seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="4ba64-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="4ba64-144">Os chamadores podem registrar para notificações sobre todo contêineres, listas de distribuição ou mensagens de usuários.</span><span class="sxs-lookup"><span data-stu-id="4ba64-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="4ba64-145">Normalmente, os clientes chame o método de [IAddrBook::Advise](iaddrbook-advise.md) para registrar para notificações do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="4ba64-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="4ba64-146">MAPI chama o método **Advise** do provedor de catálogo de endereços que é responsável pelo objeto representado pelo identificador de entrada no _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="4ba64-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="4ba64-147">Quando ocorre uma alteração ao objeto do tipo representado na _ulEventMask_indicado, é feita uma chamada para o método **OnNotify** do coletor advise apontado pela _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="4ba64-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="4ba64-148">Dados passados na estrutura de **notificação** para a rotina de **OnNotify** descrevem o evento.</span><span class="sxs-lookup"><span data-stu-id="4ba64-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4ba64-149">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="4ba64-149">Notes to implementers</span></span>

<span data-ttu-id="4ba64-150">Você pode oferecer suporte a notificação com ou sem a Ajuda de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ba64-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="4ba64-151">MAPI tem três métodos do objeto de suporte para ajudar a implementar a notificação de provedores de serviços:</span><span class="sxs-lookup"><span data-stu-id="4ba64-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="4ba64-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="4ba64-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="4ba64-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4ba64-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="4ba64-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="4ba64-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="4ba64-155">Se você optar por usar os métodos de suporte MAPI, ligue para **inscrever-se** ao seu método **Advise** é chamado e liberar o ponteiro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="4ba64-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="4ba64-156">Se você optar por suporte a notificação, chame o método de **AddRef** do coletor advise representado pelo parâmetro _lpAdviseSink_ para manter uma cópia deste ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4ba64-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="4ba64-157">Manter essa cópia até seu método [IABLogon::Unadvise](iablogon-unadvise.md) é chamado para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="4ba64-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="4ba64-158">Independentemente de como você oferecer suporte à notificação, atribua um número diferente de zero de conexão para o registro de notificação e retorná-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="4ba64-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="4ba64-159">Não libere esse número de conexão até que o método **Unadvise** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="4ba64-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4ba64-160">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4ba64-160">Notes to callers</span></span>

<span data-ttu-id="4ba64-161">O ponteiro advise do coletor de eventos que você passa no parâmetro _lpAdviseSink_ para **Advise** pode apontar para um objeto que você criou ou que MAPI criado por meio da função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba64-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="4ba64-162">Você talvez queira usar **HrThisThreadAdviseSink** se você oferecer suporte a vários threads de execução e deseja Certifique-se de que as chamadas subsequentes para seu método de **OnNotify** ocorram em um horário adequado em um segmento apropriado.</span><span class="sxs-lookup"><span data-stu-id="4ba64-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="4ba64-163">Esteja preparado para seu objeto de coletor de eventos advise ser liberada a qualquer momento após sua chamada **Advise** e antes de chamar **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="4ba64-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="4ba64-164">Portanto, você deve liberar seu objeto de coletor de eventos advise depois **Advise** retorna, a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="4ba64-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4ba64-165">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4ba64-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="4ba64-166">Para obter informações sobre como usar os métodos **IMAPISupport** para oferecer suporte a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="4ba64-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="4ba64-167">Para obter mais informações sobre multithreading e MAPI, consulte [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4ba64-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ba64-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ba64-168">See also</span></span>



[<span data-ttu-id="4ba64-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4ba64-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4ba64-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4ba64-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="4ba64-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4ba64-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4ba64-172">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="4ba64-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4ba64-173">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ba64-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

