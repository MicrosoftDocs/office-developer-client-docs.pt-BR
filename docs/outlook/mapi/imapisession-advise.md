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
# <a name="imapisessionadvise"></a><span data-ttu-id="a4cce-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="a4cce-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="a4cce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4cce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4cce-105">Registra para receber notificações de eventos específicos que afetam a sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a4cce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4cce-106">Parameters</span></span>

 <span data-ttu-id="a4cce-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4cce-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a4cce-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a4cce-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a4cce-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4cce-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a4cce-110">no Um ponteiro para o identificador de entrada do objeto do catálogo de endereços ou do repositório de mensagens sobre quais notificações devem ser geradas, ou NULL, que indica que o cliente está se registrando para receber notificações sobre eventos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="a4cce-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="a4cce-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="a4cce-112">no Uma máscara de valores que indica os tipos de eventos de notificação em que o cliente está interessado e deve ser incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="a4cce-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="a4cce-113">Se _lpEntryID_ for NULL, MAPI registrará automaticamente o cliente para eventos de erro críticos que afetam apenas a sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="a4cce-114">Quando o _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o parâmetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="a4cce-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="a4cce-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="a4cce-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="a4cce-116">Registra para notificações sobre erros graves, como memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="a4cce-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="a4cce-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="a4cce-117">fnevExtended</span></span> 
  
> <span data-ttu-id="a4cce-118">Registra para notificações sobre eventos específicos de um determinado catálogo de endereços ou provedor de mensagens sobre o desligamento de sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="a4cce-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="a4cce-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="a4cce-120">Registra as notificações sobre a chegada de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="a4cce-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="a4cce-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="a4cce-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="a4cce-122">Registra as notificações sobre a criação de um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="a4cce-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="a4cce-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="a4cce-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="a4cce-124">Registra para notificações sobre um objeto que está sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="a4cce-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="a4cce-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="a4cce-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="a4cce-126">Registra as notificações sobre um objeto que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="a4cce-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="a4cce-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="a4cce-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="a4cce-128">Registra para notificações sobre um objeto que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="a4cce-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="a4cce-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="a4cce-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="a4cce-130">Registra as notificações sobre um objeto que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="a4cce-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="a4cce-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="a4cce-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="a4cce-132">Registra as notificações sobre a conclusão de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a4cce-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="a4cce-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="a4cce-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="a4cce-134">no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a4cce-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="a4cce-135">Este objeto de coletor de aviso deve já ter sido alocado.</span><span class="sxs-lookup"><span data-stu-id="a4cce-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="a4cce-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="a4cce-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="a4cce-137">bota Um ponteiro para um número diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e a sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4cce-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a4cce-138">Return value</span></span>

<span data-ttu-id="a4cce-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4cce-139">S_OK</span></span> 
  
> <span data-ttu-id="a4cce-140">O registro foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a4cce-140">The registration was successful.</span></span>
    
<span data-ttu-id="a4cce-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a4cce-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="a4cce-142">O identificador de entrada apontado por _lpEntryID_ não representa um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="a4cce-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="a4cce-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a4cce-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a4cce-144">O provedor de serviços responsável pelo identificador de entrada apontado pelo _lpEntryID_ não oferece suporte ao tipo de eventos especificado no parâmetro _ulEventMask_ ou não dá suporte à notificação.</span><span class="sxs-lookup"><span data-stu-id="a4cce-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="a4cce-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a4cce-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="a4cce-146">O identificador de entrada indicado pelo _lpEntryID_ não pode ser manipulado por nenhum dos provedores de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="a4cce-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a4cce-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4cce-147">Remarks</span></span>

<span data-ttu-id="a4cce-148">O método **IMAPISession:: Advise** estabelece uma conexão entre o objeto de coletor de aviso do chamador, a sessão e, opcionalmente, um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="a4cce-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="a4cce-149">Essa conexão é usada para enviar notificações para o coletor de avisos quando um ou mais eventos especificados no parâmetro _ulEventMask_ ocorrem ao objeto apontado por _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="a4cce-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="a4cce-150">Quando _lpEntryID_ é nulo, o objeto de destino é a sessão e as notificações são enviadas somente para erros críticos e eventos estendidos.</span><span class="sxs-lookup"><span data-stu-id="a4cce-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="a4cce-151">Quando o _lpEntryID_ aponta para um identificador de entrada válido, o MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável.</span><span class="sxs-lookup"><span data-stu-id="a4cce-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="a4cce-152">Por exemplo, se _lpEntryID_ apontar para o identificador de entrada de uma lista de distribuição, o MAPI chamará o método [IABLogon:: Advise](iablogon-advise.md) do provedor de catálogo de endereços apropriado.</span><span class="sxs-lookup"><span data-stu-id="a4cce-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="a4cce-153">Para enviar uma notificação, o provedor de serviços ou MAPI chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos registrado.</span><span class="sxs-lookup"><span data-stu-id="a4cce-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="a4cce-154">Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.</span><span class="sxs-lookup"><span data-stu-id="a4cce-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4cce-155">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a4cce-155">Notes to callers</span></span>

<span data-ttu-id="a4cce-156">Em sistemas que dão suporte a vários threads de execução, \*\*\*\* a chamada para OnNotify também pode ocorrer em qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a4cce-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="a4cce-157">Se você precisar de garantia de que as notificações ocorrerão apenas em um determinado momento em um thread específico, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de coletor de aviso que você passa para o método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="a4cce-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="a4cce-158">Para determinar quando um cliente fez logoff, registre-se para notificações no seu provedor de serviços chamando **avisar** com _lpEntryID_ definido como nulo e _cbEntryID_ definido como 0.</span><span class="sxs-lookup"><span data-stu-id="a4cce-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="a4cce-159">Quando o logoff ocorrer, você receberá uma notificação fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="a4cce-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="a4cce-160">Após uma chamada a **Advise** ter sido bem-sucedida e antes de [IMAPISession:: Unadvise](imapisession-unadvise.md) foi chamado para cancelar o registro, libere seu objeto de coletor de aviso, a menos que você tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="a4cce-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="a4cce-161">Para obter uma visão geral do processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="a4cce-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="a4cce-162">Para obter mais informações sobre como lidar com notificações, consulte [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a4cce-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4cce-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a4cce-163">MFCMAPI reference</span></span>

<span data-ttu-id="a4cce-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4cce-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4cce-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a4cce-165">**File**</span></span>|<span data-ttu-id="a4cce-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="a4cce-166">**Function**</span></span>|<span data-ttu-id="a4cce-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a4cce-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4cce-168">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="a4cce-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="a4cce-169">CBaseDialog:: onNotification</span><span class="sxs-lookup"><span data-stu-id="a4cce-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="a4cce-170">MFCMAPI usa o método **IMAPISession:: Advise** para registrar notificações em relação à sessão.</span><span class="sxs-lookup"><span data-stu-id="a4cce-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4cce-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4cce-171">See also</span></span>



[<span data-ttu-id="a4cce-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="a4cce-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="a4cce-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a4cce-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="a4cce-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a4cce-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a4cce-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a4cce-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="a4cce-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4cce-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a4cce-177">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a4cce-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a4cce-178">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="a4cce-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

