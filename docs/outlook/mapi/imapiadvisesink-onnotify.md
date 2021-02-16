---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407358"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="9cbaa-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="9cbaa-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="9cbaa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cbaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cbaa-105">Responde a uma notificação executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="9cbaa-106">As tarefas executadas dependem do tipo de evento e do objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="9cbaa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cbaa-107">Parameters</span></span>

 <span data-ttu-id="9cbaa-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="9cbaa-108">_cNotif_</span></span>
  
> <span data-ttu-id="9cbaa-109">[in] A contagem de [estruturas NOTIFICATION](notification.md) apontadas pelo _parâmetro lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="9cbaa-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="9cbaa-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="9cbaa-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="9cbaa-111">[in] Um ponteiro para uma ou mais estruturas **de** NOTIFICAÇÃO que fornecem informações sobre os eventos que ocorreram.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9cbaa-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9cbaa-112">Return value</span></span>

<span data-ttu-id="9cbaa-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9cbaa-113">S_OK</span></span> 
  
> <span data-ttu-id="9cbaa-114">A notificação foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9cbaa-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cbaa-115">Remarks</span></span>

<span data-ttu-id="9cbaa-116">O processo de notificação começa quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para se registrar para receber uma notificação de um tipo específico para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="9cbaa-117">Um dos parâmetros para o método **Advise** é um ponteiro para um objeto sink que implementa a interface [IMAPIAdviseSink.](imapiadvisesinkiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="9cbaa-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="9cbaa-118">Quando ocorre um evento para o objeto de destino que corresponde à notificação registrada, o provedor de serviços, direta ou indiretamente através de MAPI, chama o método **OnNotify** do evento de aviso.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="9cbaa-119">A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="9cbaa-120">Em sistemas que suportam vários threads de execução, **OnNotify** pode ser chamado no mesmo thread que foi usado para registro ou em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="9cbaa-121">Os clientes podem se certificar de que a chamada **OnNotify** seja feita no mesmo  thread usado para chamar o **Advise,** criando o evento de alerta que eles passam para Advise com a função [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="9cbaa-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="9cbaa-122">O  _parâmetro lpNotifications_ aponta para uma ou mais estruturas **notification** que descrevem o que foi alterado durante o evento.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="9cbaa-123">Há um tipo diferente de estrutura **DE NOTIFICAÇÃO** para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="9cbaa-124">A tabela a seguir lista os valores usados para representar os possíveis tipos de eventos e as estruturas associadas a cada valor:</span><span class="sxs-lookup"><span data-stu-id="9cbaa-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="9cbaa-125">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-125">**Notification event type**</span></span>|<span data-ttu-id="9cbaa-126">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cbaa-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="9cbaa-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="9cbaa-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="9cbaa-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="9cbaa-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="9cbaa-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="9cbaa-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="9cbaa-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="9cbaa-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="9cbaa-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="9cbaa-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="9cbaa-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="9cbaa-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="9cbaa-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="9cbaa-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9cbaa-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="9cbaa-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9cbaa-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="9cbaa-148">Para obter informações gerais sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="9cbaa-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9cbaa-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="9cbaa-149">Notes to implementers</span></span>

<span data-ttu-id="9cbaa-150">Sua **implementação OnNotify** geralmente consiste em um ou mais blocos de código para cada tipo de notificação que você espera receber.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="9cbaa-151">Dentro desses blocos de código, execute as tarefas que você considera necessárias como resposta à notificação.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="9cbaa-152">Por exemplo, suponha que você se registre para receber notificações **fnevObjectModified** em uma pasta incluída em uma exibição de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="9cbaa-153">No bloco de código incluído no método **OnNotify** para manipular notificações **fnevObjectModified,** você pode enviar uma mensagem do Windows para a caixa de diálogo para solicitar uma exibição atualizada.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="9cbaa-154">Não modifique ou free a **estrutura NOTIFICATION** passada para **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="9cbaa-155">Os dados na estrutura são válidos apenas até **OnNotify** retornar.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9cbaa-156">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9cbaa-156">Notes to callers</span></span>

<span data-ttu-id="9cbaa-157">Quando ocorrem alterações em vários objetos, você pode notificar um sink de aviso registrado em uma única chamada para **OnNotify** ou em várias chamadas, dependendo das restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="9cbaa-158">Isso é verdadeiro independentemente das alterações ser o resultado de uma chamada de método ou várias.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="9cbaa-159">Por exemplo, uma chamada para [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="9cbaa-160">Como provedor de armazenamento de mensagens, você pode fazer uma chamada para **OnNotify** com um tipo de evento **fnevObjectModified** para a pasta de destino ou muitas chamadas, uma para cada uma afeta mensagens.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="9cbaa-161">Da mesma forma, se um cliente fizer chamadas repetidas para [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), essas chamadas poderão ser combinadas em um evento **fnevObjectModified** para a pasta ou separadas em eventos **fnevObjectCreated** individuais para cada nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="9cbaa-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9cbaa-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9cbaa-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9cbaa-163">MFCMAPI reference</span></span>

<span data-ttu-id="9cbaa-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9cbaa-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-165">**File**</span></span>|<span data-ttu-id="9cbaa-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-166">**Function**</span></span>|<span data-ttu-id="9cbaa-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9cbaa-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9cbaa-168">AdviseSink.h e AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="9cbaa-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="9cbaa-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="9cbaa-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="9cbaa-170">A classe CAdviseSink é implementada para manipular todas as notificações em MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="9cbaa-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cbaa-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbaa-171">See also</span></span>



[<span data-ttu-id="9cbaa-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9cbaa-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="9cbaa-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9cbaa-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="9cbaa-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="9cbaa-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="9cbaa-175">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="9cbaa-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9cbaa-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9cbaa-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="9cbaa-177">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9cbaa-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

