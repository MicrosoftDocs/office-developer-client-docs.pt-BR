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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767481"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="c887d-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="c887d-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="c887d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c887d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c887d-105">Registra para receber notificações de eventos especificados que afetam o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c887d-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c887d-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c887d-106">Parameters</span></span>

 <span data-ttu-id="c887d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c887d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c887d-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c887d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c887d-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c887d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c887d-110">[in] Um ponteiro para o identificador de entrada da pasta ou mensagem sobre o qual as notificações devem ser geradas ou **Nulo**.</span><span class="sxs-lookup"><span data-stu-id="c887d-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="c887d-111">Se _lpEntryID_ for definido como NULL, **Advise** registra para notificações no repositório de toda a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c887d-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="c887d-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="c887d-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="c887d-113">[in] Uma máscara de valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="c887d-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="c887d-114">Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="c887d-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="c887d-115">Estes são os valores válidos para o parâmetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="c887d-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="c887d-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="c887d-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="c887d-117">Registradores para notificações sobre erros graves, como as de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="c887d-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="c887d-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="c887d-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="c887d-119">Provedor de armazenamento de registradores para notificações sobre eventos específicos à mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="c887d-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="c887d-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="c887d-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="c887d-121">Registradores para notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="c887d-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="c887d-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="c887d-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="c887d-123">Registradores para notificações sobre a criação de uma nova pasta ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="c887d-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="c887d-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="c887d-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="c887d-125">Registradores para notificações sobre uma pasta ou uma mensagem que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="c887d-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="c887d-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="c887d-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="c887d-127">Registradores para notificações sobre uma pasta ou uma mensagem que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="c887d-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="c887d-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="c887d-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="c887d-129">Registradores para notificações sobre uma pasta ou mensagem está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="c887d-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="c887d-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="c887d-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="c887d-131">Registradores para notificações sobre uma pasta ou uma mensagem que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="c887d-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="c887d-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="c887d-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="c887d-133">Registradores para notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c887d-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="c887d-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c887d-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c887d-135">[in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c887d-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="c887d-136">Este objeto de coletor de eventos advise deve já foram alocado.</span><span class="sxs-lookup"><span data-stu-id="c887d-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="c887d-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c887d-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="c887d-138">[out] Um ponteiro para um número diferente de zero que representa a conexão entre o chamador avise o objeto coletor de eventos e a sessão.</span><span class="sxs-lookup"><span data-stu-id="c887d-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="c887d-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c887d-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c887d-140">[in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c887d-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="c887d-141">Este objeto de coletor de eventos advise deve já foram alocado.</span><span class="sxs-lookup"><span data-stu-id="c887d-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="c887d-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c887d-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="c887d-143">[out] Um ponteiro para um número diferente de zero de conexão que representa a conexão entre o chamador avise o objeto coletor de eventos e o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c887d-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c887d-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c887d-144">Return value</span></span>

<span data-ttu-id="c887d-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="c887d-145">S_OK</span></span> 
  
> <span data-ttu-id="c887d-146">O registro foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c887d-146">The registration was successful.</span></span>
    
<span data-ttu-id="c887d-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c887d-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c887d-148">O provedor de armazenamento de mensagem não suporta o registro para notificação por meio de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c887d-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c887d-149">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c887d-149">Remarks</span></span>

<span data-ttu-id="c887d-150">O método **IMsgStore::Advise** estabelece uma conexão entre o chamador do aviso de objeto coletor de eventos e o armazenamento de mensagens ou um objeto no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c887d-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="c887d-151">Essa conexão é usado para enviar notificações para o coletor de advise quando um ou mais eventos, conforme especificado no parâmetro _ulEventMask_ , ocorrem para o objeto de origem advise.</span><span class="sxs-lookup"><span data-stu-id="c887d-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="c887d-152">Quando os pontos de parâmetro _lpEntryID_ a um identificador de entrada válida, a fonte de advise é o objeto identificado por esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c887d-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="c887d-153">Quando _lpEntryID_ for NULL, a fonte de advise é o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c887d-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="c887d-154">Para enviar uma notificação, o provedor de armazenamento de mensagem ou MAPI chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos registrados advise.</span><span class="sxs-lookup"><span data-stu-id="c887d-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c887d-155">Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.</span><span class="sxs-lookup"><span data-stu-id="c887d-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c887d-156">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="c887d-156">Notes to implementers</span></span>

<span data-ttu-id="c887d-157">Você pode oferecer suporte a notificação com ou sem a Ajuda de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c887d-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="c887d-158">MAPI possui três métodos de objeto de suporte para ajudar os provedores de serviço a implementar notificação: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="c887d-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="c887d-159">Se você optar por usar os métodos de suporte MAPI, ligue para **inscrever-se** ao seu método **Advise** é chamado e liberar o ponteiro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="c887d-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="c887d-160">Se você optar por suporte a notificação, chame o método de [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) do coletor advise representado pelo parâmetro _lpAdviseSink_ para manter uma cópia deste ponteiro.</span><span class="sxs-lookup"><span data-stu-id="c887d-160">If you elect to support notification yourself, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="c887d-161">Manter essa cópia até seu método [IMsgStore::Unadvise](imsgstore-unadvise.md) é chamado para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="c887d-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="c887d-162">Independentemente de como você oferecer suporte à notificação, atribua um número diferente de zero de conexão para o registro de notificação e retorná-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="c887d-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="c887d-163">Não libere esse número de conexão até **Unadvise** foi chamado e foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c887d-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c887d-164">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c887d-164">Notes to callers</span></span>

<span data-ttu-id="c887d-165">Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer segmento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="c887d-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="c887d-166">Se você deve ter certeza de que as notificações ocorrem apenas em um momento específico em um determinado thread, chame a função de [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto coletor de eventos advise que você passa para **Advise**.</span><span class="sxs-lookup"><span data-stu-id="c887d-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="c887d-167">Após uma chamada para **Advise** teve sucesso e antes que tenha sido chamado **Unadvise** para cancelar o registro, estar preparado para o objeto coletor de eventos de advise ser liberada.</span><span class="sxs-lookup"><span data-stu-id="c887d-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="c887d-168">Você deve liberar seu objeto de coletor de eventos advise depois **Advise** retorna a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="c887d-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="c887d-169">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c887d-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="c887d-170">Para obter mais informações sobre como manipular notificações, consulte [Manipulação de notificações](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c887d-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c887d-171">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c887d-171">MFCMAPI reference</span></span>

<span data-ttu-id="c887d-172">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c887d-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c887d-173">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c887d-173">**File**</span></span>|<span data-ttu-id="c887d-174">**Function**</span><span class="sxs-lookup"><span data-stu-id="c887d-174">**Function**</span></span>|<span data-ttu-id="c887d-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c887d-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c887d-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="c887d-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="c887d-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="c887d-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="c887d-178">MFCMAPI usa o método **IMsgStore::Advise** para registrar para notificações no repositório de toda a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c887d-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c887d-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="c887d-179">See also</span></span>



[<span data-ttu-id="c887d-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c887d-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c887d-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c887d-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c887d-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c887d-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="c887d-183">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="c887d-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c887d-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c887d-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="c887d-185">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c887d-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

