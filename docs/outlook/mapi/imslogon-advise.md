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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382754"
---
# <a name="imslogonadvise"></a><span data-ttu-id="ea45b-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="ea45b-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="ea45b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea45b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea45b-105">Registra um objeto com um provedor de armazenamento de mensagem para notificações sobre alterações no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea45b-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="ea45b-106">O armazenamento de mensagens, em seguida, enviará notificações sobre alterações ao objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="ea45b-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ea45b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea45b-107">Parameters</span></span>

 <span data-ttu-id="ea45b-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ea45b-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="ea45b-109">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ea45b-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ea45b-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ea45b-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="ea45b-111">[in] Um ponteiro para o identificador de entrada do objeto notificações sobre quais devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="ea45b-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="ea45b-112">Este objeto pode ser uma pasta, uma mensagem ou qualquer outro objeto no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea45b-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="ea45b-113">Como alternativa, se MAPI define o parâmetro _cbEntryID_ como 0 e passa **Nulo** para _lpEntryID_, o coletor de eventos advise fornece notificações sobre alterações no repositório de toda a mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea45b-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="ea45b-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="ea45b-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="ea45b-115">[in] Uma máscara de evento dos tipos de eventos de notificação que ocorrem para o objeto sobre quais MAPI irá gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="ea45b-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="ea45b-116">A máscara filtra casos específicos.</span><span class="sxs-lookup"><span data-stu-id="ea45b-116">The mask filters specific cases.</span></span> <span data-ttu-id="ea45b-117">Cada tipo de evento tem uma estrutura associada a ela que contém informações adicionais sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="ea45b-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="ea45b-118">A tabela a seguir lista os tipos de evento possíveis, juntamente com suas estruturas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="ea45b-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="ea45b-119">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="ea45b-119">**Notification event type**</span></span>|<span data-ttu-id="ea45b-120">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="ea45b-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea45b-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="ea45b-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="ea45b-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="ea45b-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="ea45b-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="ea45b-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="ea45b-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="ea45b-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="ea45b-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="ea45b-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="ea45b-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="ea45b-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="ea45b-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="ea45b-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="ea45b-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="ea45b-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="ea45b-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="ea45b-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="ea45b-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="ea45b-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="ea45b-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="ea45b-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="ea45b-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ea45b-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ea45b-140">[in] Um ponteiro para um objeto de coletor de eventos advise a ser chamado quando ocorre um evento para o objeto de sessão notificação sobre quais tiver sido solicitada.</span><span class="sxs-lookup"><span data-stu-id="ea45b-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="ea45b-141">Este objeto de coletor de eventos advise já deve existir.</span><span class="sxs-lookup"><span data-stu-id="ea45b-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="ea45b-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ea45b-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="ea45b-143">[out] Um ponteiro para uma variável que contém o número de conexão para o registro de notificação após um retorno bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ea45b-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="ea45b-144">O número de conexão deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ea45b-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea45b-145">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ea45b-145">Return value</span></span>

<span data-ttu-id="ea45b-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea45b-146">S_OK</span></span> 
  
> <span data-ttu-id="ea45b-147">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ea45b-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ea45b-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ea45b-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ea45b-149">A operação não é suportada por MAPI ou por um ou mais provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea45b-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea45b-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea45b-150">Remarks</span></span>

<span data-ttu-id="ea45b-151">Provedores de armazenamento de mensagem implementam o método **IMSLogon::Advise** para registrar um objeto para retornos de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="ea45b-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="ea45b-152">Sempre que ocorre uma alteração no objeto indicado, o provedor verifica quais bits de máscara de evento foi definida no parâmetro _ulEventMask_ e, portanto, o tipo de alteração que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ea45b-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="ea45b-153">Se um pouco estiver definida, o provedor chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise indicado pelo parâmetro _lpAdviseSink_ para relatar o evento.</span><span class="sxs-lookup"><span data-stu-id="ea45b-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="ea45b-154">Dados passados na estrutura de notificação para a rotina de **OnNotify** descrevem o evento.</span><span class="sxs-lookup"><span data-stu-id="ea45b-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="ea45b-155">A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento posterior.</span><span class="sxs-lookup"><span data-stu-id="ea45b-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="ea45b-156">Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento.</span><span class="sxs-lookup"><span data-stu-id="ea45b-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="ea45b-157">Para manipular com segurança uma chamada para **OnNotify** que pode acontecer momento inoportunos, um aplicativo cliente deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="ea45b-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="ea45b-158">Para fornecer notificações, o provedor de armazenamento de mensagem que implementa as necessidades de **Advise** manter uma cópia do ponteiro para o _lpAdviseSink_ avise o objeto coletor de eventos; Para fazer isso, o provedor chama o método de [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para o coletor de eventos advise manter seu indicador de objeto até que o registro de notificação será cancelado com uma chamada ao método [IMSLogon::Unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="ea45b-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="ea45b-159">A implementação de **Advise** deve atribuir um número de conexão para o registro de notificação e chamar **AddRef** este número de conexão antes de retorná-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="ea45b-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ea45b-160">Provedores de serviços podem liberar o objeto coletor de eventos advise antes que o registro será cancelado, mas eles não devem liberar o número de conexão até que tenha sido chamado **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="ea45b-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="ea45b-161">Depois que uma chamada para **Advise** teve sucesso e antes de **Unadvise** tiver sido chamado, provedores devem ser preparados para o objeto coletor de eventos de advise ser liberada.</span><span class="sxs-lookup"><span data-stu-id="ea45b-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ea45b-162">Portanto, um provedor deve liberar seu objeto de coletor advise depois **Advise** retorna, a menos que ele tem um uso específico de longo prazo para que ele.</span><span class="sxs-lookup"><span data-stu-id="ea45b-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ea45b-163">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ea45b-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ea45b-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea45b-164">See also</span></span>



[<span data-ttu-id="ea45b-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ea45b-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ea45b-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ea45b-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ea45b-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ea45b-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="ea45b-168">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea45b-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ea45b-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea45b-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

