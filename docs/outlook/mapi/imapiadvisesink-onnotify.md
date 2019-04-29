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
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="d9014-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d9014-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="d9014-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9014-105">Responde a uma notificação executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="d9014-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="d9014-106">As tarefas realizadas dependem do tipo de evento e do objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="d9014-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="d9014-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9014-107">Parameters</span></span>

 <span data-ttu-id="d9014-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="d9014-108">_cNotif_</span></span>
  
> <span data-ttu-id="d9014-109">no A contagem de estruturas de [notificação](notification.md) apontadas pelo parâmetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="d9014-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="d9014-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="d9014-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="d9014-111">no Um ponteiro para uma ou mais estruturas de **notificação** que fornecem informações sobre os eventos que ocorreram.</span><span class="sxs-lookup"><span data-stu-id="d9014-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9014-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d9014-112">Return value</span></span>

<span data-ttu-id="d9014-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9014-113">S_OK</span></span> 
  
> <span data-ttu-id="d9014-114">A notificação foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d9014-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9014-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9014-115">Remarks</span></span>

<span data-ttu-id="d9014-116">O processo de notificação é iniciado quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para se registrar para receber uma notificação de um tipo específico para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="d9014-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="d9014-117">Um dos parâmetros para o método **Advise** é um ponteiro para um objeto de coletor de aviso que implementa a interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="d9014-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="d9014-118">Quando ocorre um evento para o objeto de destino que corresponde à notificação registrada, o provedor de serviços, direta ou indiretamente por meio de MAPI, chama \*\*\*\* o método OnNotify do coletor de avisos.</span><span class="sxs-lookup"><span data-stu-id="d9014-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="d9014-119">A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior.</span><span class="sxs-lookup"><span data-stu-id="d9014-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="d9014-120">Em sistemas que oferecem suporte a vários threads \*\*\*\* de execução, OnNotify pode ser chamado no mesmo thread que foi usado para registro ou em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="d9014-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="d9014-121">Os clientes podem garantir que a \*\*\*\* chamada OnNotify seja feita no mesmo thread usado para chamar **Advise** , criando o coletor de avisos que eles passam para **avisar** com a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="d9014-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="d9014-122">O parâmetro _lpNotifications_ aponta para uma ou mais estruturas de **notificação** que descrevem o que foi alterado durante o evento.</span><span class="sxs-lookup"><span data-stu-id="d9014-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="d9014-123">Há um tipo diferente de estrutura de **notificação** para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="d9014-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="d9014-124">A tabela a seguir lista os valores que são usados para representar os possíveis tipos de eventos e as estruturas associadas a cada valor:</span><span class="sxs-lookup"><span data-stu-id="d9014-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="d9014-125">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="d9014-125">**Notification event type**</span></span>|<span data-ttu-id="d9014-126">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="d9014-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9014-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="d9014-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="d9014-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="d9014-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="d9014-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="d9014-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="d9014-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="d9014-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="d9014-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d9014-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="d9014-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="d9014-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d9014-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="d9014-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="d9014-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d9014-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="d9014-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="d9014-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d9014-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="d9014-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="d9014-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d9014-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="d9014-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="d9014-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="d9014-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="d9014-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="d9014-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="d9014-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="d9014-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="d9014-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d9014-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="d9014-147">Para obter mais informações sobre como configurar e interromper notificações, consulte as entradas de referência para os métodos **Advise** e **Unadvise** para qualquer uma das seguintes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [](imapitableiunknown.md)IMAPITable, [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d9014-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="d9014-148">Para obter informações gerais sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d9014-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9014-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="d9014-149">Notes to implementers</span></span>

<span data-ttu-id="d9014-150">A \*\*\*\* implementação onnotificar normalmente consiste em um ou mais blocos de código para cada tipo de notificação que você espera receber.</span><span class="sxs-lookup"><span data-stu-id="d9014-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="d9014-151">Nesses blocos de código, execute quaisquer tarefas que você considere necessárias como resposta à notificação.</span><span class="sxs-lookup"><span data-stu-id="d9014-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="d9014-152">Por exemplo, suponha que você se registre para receber notificações do **fnevObjectModified** em uma pasta incluída em uma caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="d9014-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="d9014-153">No bloco de código que você inclui no seu método **OnNotify** para manipular notificações do **fnevObjectModified** , você pode enviar uma mensagem do Windows para a caixa de diálogo para solicitar uma exibição atualizada.</span><span class="sxs-lookup"><span data-stu-id="d9014-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="d9014-154">Não modifique nem libere a estrutura de **notificação** passada para **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="d9014-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="d9014-155">Os dados na estrutura são válidos somente até que **OnNotify** Returns seja retornado.</span><span class="sxs-lookup"><span data-stu-id="d9014-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9014-156">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d9014-156">Notes to callers</span></span>

<span data-ttu-id="d9014-157">Quando ocorrem alterações em vários objetos, você pode notificar um coletor de aviso registrado em uma única \*\*\*\* chamada para OnNotify ou em várias chamadas, dependendo das restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="d9014-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="d9014-158">Isso é verdadeiro independentemente se as alterações são o resultado de uma chamada de método ou várias.</span><span class="sxs-lookup"><span data-stu-id="d9014-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="d9014-159">Por exemplo, uma chamada para [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="d9014-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="d9014-160">Como um provedor de armazenamento de mensagens, você pode fazer uma \*\*\*\* chamada para onnotificar com um tipo de evento **fnevObjectModified** para a pasta de destino ou muitas chamadas, uma para cada uma das mensagens afetadas.</span><span class="sxs-lookup"><span data-stu-id="d9014-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="d9014-161">Da mesma forma, se um cliente fizer chamadas repetidas para [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), essas chamadas poderão ser combinadas em um evento **fnevObjectModified** para a pasta ou separados em eventos **fnevObjectCreated** individuais para cada nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="d9014-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="d9014-162">Para obter mais informações sobre como e quando gerar notificações, consulte [Event Notification in MAPI](event-notification-in-mapi.md) and [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="d9014-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9014-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9014-163">MFCMAPI reference</span></span>

<span data-ttu-id="d9014-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9014-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9014-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d9014-165">**File**</span></span>|<span data-ttu-id="d9014-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="d9014-166">**Function**</span></span>|<span data-ttu-id="d9014-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="d9014-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9014-168">AdviseSink. h e AdviseSink. cpp</span><span class="sxs-lookup"><span data-stu-id="d9014-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="d9014-169">CAdviseSink:: OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="d9014-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="d9014-170">A classe CAdviseSink é implementada para lidar com todas as notificações no MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="d9014-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9014-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9014-171">See also</span></span>



[<span data-ttu-id="d9014-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d9014-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="d9014-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d9014-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="d9014-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="d9014-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="d9014-175">Notifica</span><span class="sxs-lookup"><span data-stu-id="d9014-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d9014-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9014-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="d9014-177">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d9014-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

