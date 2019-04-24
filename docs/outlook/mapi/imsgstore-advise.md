---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317322"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="4f0dd-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="4f0dd-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="4f0dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f0dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f0dd-105">Registra para receber notificações de eventos específicos que afetam o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4f0dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f0dd-106">Parameters</span></span>

 <span data-ttu-id="4f0dd-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4f0dd-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4f0dd-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4f0dd-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4f0dd-110">no Um ponteiro para o identificador de entrada da pasta ou da mensagem sobre a qual as notificações devem ser geradas ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="4f0dd-111">Se _lpEntryID_ estiver definido como nulo, **avisará** os registros para notificações em todo o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="4f0dd-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="4f0dd-113">no Uma máscara de valores que indica os tipos de eventos de notificação nos quais o chamador está interessado e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="4f0dd-114">Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="4f0dd-115">Estes são os valores válidos para o parâmetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="4f0dd-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="4f0dd-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="4f0dd-117">Registra para notificações sobre erros graves, como memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="4f0dd-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="4f0dd-119">Registra as notificações sobre eventos específicos para o provedor de armazenamento de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="4f0dd-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="4f0dd-121">Registra as notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="4f0dd-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="4f0dd-123">Registra para notificações sobre a criação de uma nova pasta ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="4f0dd-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="4f0dd-125">Registra para notificações sobre uma pasta ou mensagem que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="4f0dd-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="4f0dd-127">Registra para notificações sobre uma pasta ou mensagem que está sendo excluída.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="4f0dd-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="4f0dd-129">Registra para notificações sobre uma pasta ou mensagem que está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="4f0dd-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="4f0dd-131">Registra para notificações sobre uma pasta ou mensagem que está sendo movida.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="4f0dd-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="4f0dd-133">Registra as notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="4f0dd-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4f0dd-135">no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="4f0dd-136">Este objeto de coletor de aviso deve já ter sido alocado.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="4f0dd-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="4f0dd-138">bota Um ponteiro para um número diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e a sessão.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="4f0dd-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4f0dd-140">no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="4f0dd-141">Este objeto de coletor de aviso deve já ter sido alocado.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="4f0dd-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4f0dd-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="4f0dd-143">bota Um ponteiro para um número de conexão diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f0dd-144">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4f0dd-144">Return value</span></span>

<span data-ttu-id="4f0dd-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f0dd-145">S_OK</span></span> 
  
> <span data-ttu-id="4f0dd-146">O registro foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-146">The registration was successful.</span></span>
    
<span data-ttu-id="4f0dd-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4f0dd-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4f0dd-148">O provedor de repositório de mensagens não oferece suporte ao registro de notificação por meio do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f0dd-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f0dd-149">Remarks</span></span>

<span data-ttu-id="4f0dd-150">O método **IMsgStore:: Advise** estabelece uma conexão entre o objeto de coletor de aviso do chamador e o repositório de mensagens ou um objeto no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="4f0dd-151">Essa conexão é usada para enviar notificações ao coletor de avisos quando um ou mais eventos, conforme especificado no parâmetro _ulEventMask_ , ocorrem no objeto de origem de aviso.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="4f0dd-152">Quando o parâmetro _lpEntryID_ aponta para um identificador de entrada válido, a fonte de aviso é o objeto identificado por esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="4f0dd-153">Quando _lpEntryID_ é nulo, a fonte de aviso é o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="4f0dd-154">Para enviar uma notificação, o provedor de armazenamento de mensagens ou MAPI chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos registrado.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="4f0dd-155">Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4f0dd-156">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="4f0dd-156">Notes to implementers</span></span>

<span data-ttu-id="4f0dd-157">Você pode dar suporte à notificação com ou sem a ajuda do MAPI.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="4f0dd-158">O MAPI tem três métodos de objeto de suporte para ajudar os provedores de serviços a implementar a notificação: [IMAPISupport:: Subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport:: Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="4f0dd-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="4f0dd-159">Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando seu método **Advise** for chamado e libere o ponteiro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="4f0dd-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="4f0dd-160">Se você optar por dar suporte a uma notificação por conta própria, chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) do coletor de avisos representado pelo parâmetro _lpAdviseSink_ para manter uma cópia desse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="4f0dd-161">Mantenha essa cópia até que o método [IMsgStore:: Unadvise](imsgstore-unadvise.md) seja chamado para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="4f0dd-162">Independentemente de como você dá suporte à notificação, atribua um número de conexão diferente de zero para o registro de notificação e devolva-o no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="4f0dd-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="4f0dd-163">Não libera esse número de conexão até que **Unadvise** seja chamado e concluído.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f0dd-164">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4f0dd-164">Notes to callers</span></span>

<span data-ttu-id="4f0dd-165">Em sistemas que dão suporte a vários threads de execução, \*\*\*\* a chamada para OnNotify também pode ocorrer em qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="4f0dd-166">Se você precisa ter certeza de que as notificações ocorrem somente em um determinado momento em um thread específico, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de coletor de aviso que você passa para **avisar**.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="4f0dd-167">Após uma chamada para **Advise** ter sido bem-sucedida e antes que **Unadvise** seja chamado para cancelar o registro, esteja preparado para o objeto de coletor de aviso a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="4f0dd-168">Você deve liberar seu objeto de coletor de aviso após o **aviso de alerta** , a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4f0dd-169">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4f0dd-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="4f0dd-170">Para obter mais informações sobre como lidar com notificações, consulte [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4f0dd-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4f0dd-171">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4f0dd-171">MFCMAPI reference</span></span>

<span data-ttu-id="4f0dd-172">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4f0dd-173">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4f0dd-173">**File**</span></span>|<span data-ttu-id="4f0dd-174">**Função**</span><span class="sxs-lookup"><span data-stu-id="4f0dd-174">**Function**</span></span>|<span data-ttu-id="4f0dd-175">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="4f0dd-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f0dd-176">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="4f0dd-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="4f0dd-177">CBaseDialog:: onNotification</span><span class="sxs-lookup"><span data-stu-id="4f0dd-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="4f0dd-178">MFCMAPI usa o método **IMsgStore:: Advise** para registrar notificações em todo o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f0dd-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f0dd-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f0dd-179">See also</span></span>



[<span data-ttu-id="4f0dd-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4f0dd-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4f0dd-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4f0dd-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4f0dd-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4f0dd-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="4f0dd-183">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4f0dd-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4f0dd-184">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4f0dd-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="4f0dd-185">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4f0dd-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

