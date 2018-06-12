---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767184"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="f8cb3-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="f8cb3-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="f8cb3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8cb3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8cb3-105">Registra para receber notificações de eventos especificados que afetam a sessão.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f8cb3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f8cb3-106">Parameters</span></span>

 <span data-ttu-id="f8cb3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8cb3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f8cb3-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f8cb3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f8cb3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8cb3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f8cb3-110">[in] Um ponteiro para o identificador de entrada do catálogo de endereços ou objeto de repositório de mensagem notificações sobre quais devem ser geradas ou nulo, o que indica que o cliente está registrando para receber notificações de eventos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="f8cb3-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f8cb3-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="f8cb3-112">[in] Uma máscara de valores que indicam os tipos de eventos de notificação que o cliente está interessado em e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="f8cb3-113">Se _lpEntryID_ for NULL, MAPI registra automaticamente o cliente para eventos de erros críticos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="f8cb3-114">Quando _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o parâmetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="f8cb3-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="f8cb3-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="f8cb3-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="f8cb3-116">Registradores para notificações sobre erros graves, como as de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="f8cb3-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="f8cb3-117">fnevExtended</span></span> 
  
> <span data-ttu-id="f8cb3-118">Registradores notificações sobre eventos específicos a um catálogo de endereços particular ou mensagem de provedor de armazenamento e sobre sessão desligado.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="f8cb3-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="f8cb3-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="f8cb3-120">Registradores para notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="f8cb3-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="f8cb3-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="f8cb3-122">Registradores para notificações sobre a criação de um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="f8cb3-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="f8cb3-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="f8cb3-124">Registradores para notificações sobre um objeto que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="f8cb3-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="f8cb3-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="f8cb3-126">Registradores para notificações sobre um objeto que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="f8cb3-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="f8cb3-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="f8cb3-128">Registradores para notificações sobre um objeto que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="f8cb3-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="f8cb3-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="f8cb3-130">Registradores para notificações sobre um objeto que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="f8cb3-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="f8cb3-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="f8cb3-132">Registradores para notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="f8cb3-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f8cb3-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f8cb3-134">[in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f8cb3-135">Este objeto de coletor de eventos advise deve já foram alocado.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="f8cb3-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f8cb3-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="f8cb3-137">[out] Um ponteiro para um número diferente de zero que representa a conexão entre o chamador avise o objeto coletor de eventos e a sessão.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8cb3-138">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8cb3-138">Return value</span></span>

<span data-ttu-id="f8cb3-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8cb3-139">S_OK</span></span> 
  
> <span data-ttu-id="f8cb3-140">O registro foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-140">The registration was successful.</span></span>
    
<span data-ttu-id="f8cb3-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f8cb3-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="f8cb3-142">O identificador de entrada apontado pela _lpEntryID_ não representa um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="f8cb3-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f8cb3-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f8cb3-144">O provedor de serviços para o identificador de entrada apontado pela _lpEntryID_ responsável não suporta o tipo de eventos especificado no parâmetro _ulEventMask_ ou não oferece suporte a notificação.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="f8cb3-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f8cb3-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f8cb3-146">O identificador de entrada apontado pela _lpEntryID_ não pode ser manipulado por qualquer um dos provedores de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f8cb3-147">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="f8cb3-147">Remarks</span></span>

<span data-ttu-id="f8cb3-148">O método **IMAPISession::Advise** estabelece uma conexão entre o chamador do objeto de coletor de eventos, a sessão e, opcionalmente, um provedor de serviços de aviso.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="f8cb3-149">Essa conexão é usado para enviar notificações para o coletor de advise quando um ou mais eventos especificados no parâmetro _ulEventMask_ ocorrem ao objeto apontado pela _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="f8cb3-150">Quando _lpEntryID_ for NULL, o objeto de destino é a sessão e notificações serão enviadas somente para erros críticos e eventos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="f8cb3-151">Quando _lpEntryID_ aponta para um identificador de entrada válida, MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="f8cb3-152">Por exemplo, se _lpEntryID_ aponta para o identificador de entrada de uma lista de distribuição, MAPI chama o método de [IABLogon::Advise](iablogon-advise.md) do provedor de catálogo de endereço apropriado.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="f8cb3-153">Para enviar uma notificação, o provedor de serviços ou o MAPI chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos registrados advise.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="f8cb3-154">Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8cb3-155">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f8cb3-155">Notes to callers</span></span>

<span data-ttu-id="f8cb3-156">Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer segmento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="f8cb3-157">Se você precisar de garantia de que as notificações ocorrerá apenas em um momento específico em um determinado thread, chame a função de [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto coletor de eventos advise que você passa para o método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="f8cb3-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="f8cb3-158">Para determinar quando um cliente tiverem feito logoff, registre-se para notificações no seu provedor de serviço chamando **Advise** com _lpEntryID_ definido como NULL e _cbEntryID_ definida como 0.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="f8cb3-159">Quando o logoff ocorre, você receberá uma notificação fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="f8cb3-160">Depois que uma chamada para **Advise** teve sucesso e antes de [IMAPISession::Unadvise](imapisession-unadvise.md) tiver sido chamado para cancelar o registro, libere seu objeto de coletor de eventos advise a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f8cb3-161">Para obter uma visão geral do processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb3-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="f8cb3-162">Para obter mais informações sobre como manipular notificações, consulte [Manipulação de notificações](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb3-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8cb3-163">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f8cb3-163">MFCMAPI reference</span></span>

<span data-ttu-id="f8cb3-164">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8cb3-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f8cb3-165">**File**</span></span>|<span data-ttu-id="f8cb3-166">**Function**</span><span class="sxs-lookup"><span data-stu-id="f8cb3-166">**Function**</span></span>|<span data-ttu-id="f8cb3-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f8cb3-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8cb3-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="f8cb3-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="f8cb3-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="f8cb3-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="f8cb3-170">MFCMAPI usa o método **IMAPISession::Advise** para registrar para notificações contra a sessão.</span><span class="sxs-lookup"><span data-stu-id="f8cb3-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8cb3-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8cb3-171">See also</span></span>



[<span data-ttu-id="f8cb3-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f8cb3-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="f8cb3-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f8cb3-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f8cb3-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f8cb3-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f8cb3-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f8cb3-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="f8cb3-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8cb3-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f8cb3-177">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f8cb3-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f8cb3-178">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="f8cb3-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

