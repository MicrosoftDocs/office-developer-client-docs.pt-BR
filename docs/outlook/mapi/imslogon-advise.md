---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317308"
---
# <a name="imslogonadvise"></a><span data-ttu-id="f1385-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f1385-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="f1385-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1385-105">Registra um objeto com um provedor de repositório de mensagens para notificações sobre alterações no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f1385-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="f1385-106">O repositório de mensagens enviará notificações sobre alterações no objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="f1385-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f1385-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1385-107">Parameters</span></span>

 <span data-ttu-id="f1385-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f1385-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="f1385-109">no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f1385-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f1385-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f1385-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="f1385-111">no Um ponteiro para o identificador de entrada do objeto sobre quais notificações devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="f1385-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="f1385-112">Este objeto pode ser uma pasta, uma mensagem ou qualquer outro objeto no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f1385-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="f1385-113">Como alternativa, se MAPI define o parâmetro _cbEntryID_ como 0 e passa **NULL** para _lpEntryID_, o coletor de avisos fornece notificações sobre alterações em todo o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f1385-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="f1385-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f1385-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="f1385-115">no Uma máscara de evento dos tipos de eventos de notificação que ocorrem para o objeto sobre o qual o MAPI irá gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="f1385-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="f1385-116">A máscara filtra casos específicos.</span><span class="sxs-lookup"><span data-stu-id="f1385-116">The mask filters specific cases.</span></span> <span data-ttu-id="f1385-117">Cada tipo de evento tem uma estrutura associada a ele que contém informações adicionais sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="f1385-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="f1385-118">A tabela a seguir lista os possíveis tipos de evento juntamente com suas estruturas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f1385-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="f1385-119">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="f1385-119">**Notification event type**</span></span>|<span data-ttu-id="f1385-120">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="f1385-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1385-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="f1385-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="f1385-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="f1385-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="f1385-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="f1385-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="f1385-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="f1385-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="f1385-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="f1385-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="f1385-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="f1385-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="f1385-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="f1385-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="f1385-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="f1385-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="f1385-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="f1385-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="f1385-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f1385-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="f1385-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="f1385-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="f1385-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f1385-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f1385-140">no Um ponteiro para um objeto de coletor de aviso a ser chamado quando ocorre um evento para o objeto Session sobre o qual a notificação foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="f1385-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="f1385-141">Este objeto de coletor de aviso já deve existir.</span><span class="sxs-lookup"><span data-stu-id="f1385-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="f1385-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f1385-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="f1385-143">bota Um ponteiro para uma variável que em um retorno bem-sucedido contém o número de conexão para o registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="f1385-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="f1385-144">O número de conexão deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f1385-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1385-145">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f1385-145">Return value</span></span>

<span data-ttu-id="f1385-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1385-146">S_OK</span></span> 
  
> <span data-ttu-id="f1385-147">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f1385-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f1385-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f1385-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f1385-149">A operação não é suportada pelo MAPI ou por um ou mais provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="f1385-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1385-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1385-150">Remarks</span></span>

<span data-ttu-id="f1385-151">Os provedores de repositórios de mensagens implementam o método **IMSLogon:: Advise** para registrar um objeto para retornos de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="f1385-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="f1385-152">Sempre que uma alteração ocorre no objeto indicado, o provedor verifica se o bit de máscara de evento foi definido no parâmetro _ulEventMask_ e, portanto, que tipo de alteração ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f1385-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="f1385-153">Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o objeto de coletor de aviso indicado pelo parâmetro _lpAdviseSink_ para relatar o evento.</span><span class="sxs-lookup"><span data-stu-id="f1385-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="f1385-154">Dados passados na estrutura de notificação para a \*\*\*\* rotina OnNotify descreve o evento.</span><span class="sxs-lookup"><span data-stu-id="f1385-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="f1385-155">A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou em qualquer momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f1385-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="f1385-156">Em sistemas que oferecem suporte a vários threads de execução, \*\*\*\* a chamada para OnNotify pode ocorrer em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="f1385-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="f1385-157">Para lidar com segurança uma chamada para \*\*\*\* onnotificar que pode ocorrer em um momento de inopportune, um aplicativo cliente deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="f1385-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="f1385-158">Para fornecer notificações, o provedor de repositório de mensagens que implementa o **aviso** precisa manter uma cópia do ponteiro para o objeto de coletor de aviso _lpAdviseSink_ ; para fazer isso, o provedor chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para o coletor de avisos para manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método [IMSLogon:: Unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="f1385-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="f1385-159">A implementação de **aviso** deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de devolvê-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="f1385-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f1385-160">Os provedores de serviços podem liberar o objeto de coletor de aviso antes de o registro ser cancelado, mas não devem liberar o número de conexão até que **Unadvise** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f1385-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="f1385-161">Após uma chamada a **Advise** ter sido bem-sucedida e antes que **Unadvise** seja chamado, os provedores devem estar preparados para que o objeto de coletor de aviso seja liberado.</span><span class="sxs-lookup"><span data-stu-id="f1385-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="f1385-162">Portanto, um provedor deve liberar seu objeto de coletor de aviso depois que **Advise** retornar, a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="f1385-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f1385-163">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f1385-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1385-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1385-164">See also</span></span>



[<span data-ttu-id="f1385-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f1385-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f1385-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f1385-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f1385-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f1385-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="f1385-168">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1385-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f1385-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1385-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

