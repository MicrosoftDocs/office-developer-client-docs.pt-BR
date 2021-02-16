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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419832"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="1c9bd-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="1c9bd-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="1c9bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c9bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c9bd-105">Registra para receber notificação de eventos especificados que afetam a sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1c9bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c9bd-106">Parameters</span></span>

 <span data-ttu-id="1c9bd-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1c9bd-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="1c9bd-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1c9bd-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1c9bd-110">[in] Um ponteiro para o identificador de entrada do livro de endereços ou objeto do armazenamento de mensagens sobre o qual as notificações devem ser geradas, ou NULL, que indica que o cliente está se registrando para receber notificações sobre eventos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="1c9bd-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="1c9bd-112">[in] Uma máscara de valores que indicam os tipos de eventos de notificação nos quais o cliente está interessado e devem ser incluídos no registro.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="1c9bd-113">Se  _lpEntryID_ for NULL, MAPI registrará automaticamente o cliente para eventos de erro críticos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="1c9bd-114">Quando _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o _parâmetro ulEventMask:_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="1c9bd-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="1c9bd-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="1c9bd-116">Registra notificações sobre erros graves, como memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="1c9bd-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="1c9bd-117">fnevExtended</span></span> 
  
> <span data-ttu-id="1c9bd-118">Registra notificações sobre eventos específicos de um determinado address book ou provedor de armazenamento de mensagens e sobre o desligar da sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="1c9bd-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="1c9bd-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="1c9bd-120">Registra notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="1c9bd-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="1c9bd-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="1c9bd-122">Registra notificações sobre a criação de um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="1c9bd-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="1c9bd-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="1c9bd-124">Registra notificações sobre um objeto sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="1c9bd-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="1c9bd-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="1c9bd-126">Registra notificações sobre um objeto que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="1c9bd-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="1c9bd-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="1c9bd-128">Registra notificações sobre um objeto que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="1c9bd-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="1c9bd-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="1c9bd-130">Registra notificações sobre um objeto que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="1c9bd-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="1c9bd-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="1c9bd-132">Registra notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="1c9bd-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="1c9bd-134">[in] Um ponteiro para um objeto sink de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="1c9bd-135">Esse objeto sink de aconselhmento já deve ter sido alocado.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="1c9bd-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="1c9bd-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="1c9bd-137">[out] Um ponteiro para um número que não seja zero que representa a conexão entre o objeto sink de alerta do chamador e a sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c9bd-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1c9bd-138">Return value</span></span>

<span data-ttu-id="1c9bd-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c9bd-139">S_OK</span></span> 
  
> <span data-ttu-id="1c9bd-140">O registro foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-140">The registration was successful.</span></span>
    
<span data-ttu-id="1c9bd-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1c9bd-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="1c9bd-142">O identificador de entrada apontado por  _lpEntryID_ não representa um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="1c9bd-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1c9bd-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1c9bd-144">O provedor de serviços responsável pelo identificador de entrada apontado por  _lpEntryID_ não suporta o tipo de eventos especificados no parâmetro  _ulEventMask_ ou não suporta notificação.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="1c9bd-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1c9bd-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1c9bd-146">O identificador de entrada apontado por  _lpEntryID_ não pode ser manipulado por nenhum dos provedores de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c9bd-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c9bd-147">Remarks</span></span>

<span data-ttu-id="1c9bd-148">O **método IMAPISession::Advise** estabelece uma conexão entre o objeto sink de alerta do chamador, a sessão e, opcionalmente, um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="1c9bd-149">Essa conexão é usada para enviar notificações ao sink de aviso quando um ou mais eventos especificados no  _parâmetro ulEventMask_ ocorrem para o objeto apontado por  _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="1c9bd-150">Quando  _lpEntryID_ é NULL, o objeto de destino é a sessão e as notificações são enviadas apenas para erros críticos e eventos estendidos.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="1c9bd-151">Quando  _lpEntryID_ aponta para um identificador de entrada válido, MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="1c9bd-152">Por exemplo, se  _lpEntryID_ aponta para o identificador de entrada de uma lista de distribuição, o MAPI chama o método [IABLogon::Advise](iablogon-advise.md) do provedor de endereços apropriado.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="1c9bd-153">Para enviar uma notificação, o provedor de serviços ou o MAPI chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do pia registrado.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="1c9bd-154">Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1c9bd-155">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1c9bd-155">Notes to callers</span></span>

<span data-ttu-id="1c9bd-156">Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="1c9bd-157">Se você precisar de garantia de que as notificações ocorrerão apenas em um determinado momento em um determinado thread, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de evento de aviso que você passa para o método **Advise.**</span><span class="sxs-lookup"><span data-stu-id="1c9bd-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="1c9bd-158">Para determinar quando um cliente fez logon, registre-se para notificações em seu provedor de serviços chamando **Advise** com  _lpEntryID_ definido como NULL e  _cbEntryID_ definido como 0.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="1c9bd-159">Quando o logoff ocorrer, você receberá uma notificação fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="1c9bd-160">Depois que uma chamada para o **Advise** tiver sido bem-sucedida e antes de [IMAPISession::Unadvise](imapisession-unadvise.md) ter sido chamado para cancelar o registro, libere seu objeto de cliente a menos que você tenha um uso específico a longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="1c9bd-161">Para uma visão geral do processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="1c9bd-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="1c9bd-162">Para obter mais informações sobre como lidar com notificações, consulte [Manipulando notificações.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="1c9bd-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c9bd-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1c9bd-163">MFCMAPI reference</span></span>

<span data-ttu-id="1c9bd-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c9bd-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1c9bd-165">**File**</span></span>|<span data-ttu-id="1c9bd-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="1c9bd-166">**Function**</span></span>|<span data-ttu-id="1c9bd-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1c9bd-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c9bd-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="1c9bd-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="1c9bd-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="1c9bd-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="1c9bd-170">MFCMAPI usa o **método IMAPISession::Advise** para se registrar para notificações contra a sessão.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c9bd-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c9bd-171">See also</span></span>



[<span data-ttu-id="1c9bd-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="1c9bd-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="1c9bd-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1c9bd-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="1c9bd-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1c9bd-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="1c9bd-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1c9bd-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="1c9bd-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c9bd-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1c9bd-177">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1c9bd-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1c9bd-178">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="1c9bd-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

