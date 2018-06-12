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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766927"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="4216a-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4216a-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="4216a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4216a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4216a-105">Responde a uma notificação, executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="4216a-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="4216a-106">As tarefas realizadas dependem do tipo de evento e o objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="4216a-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="4216a-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4216a-107">Parameters</span></span>

 <span data-ttu-id="4216a-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="4216a-108">_cNotif_</span></span>
  
> <span data-ttu-id="4216a-109">[in] A contagem de estruturas de [notificação](notification.md) apontado pelo parâmetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="4216a-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="4216a-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="4216a-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="4216a-111">[in] Um ponteiro para uma ou mais estruturas de **notificação** que fornecem informações sobre os eventos que ocorreram.</span><span class="sxs-lookup"><span data-stu-id="4216a-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4216a-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4216a-112">Return value</span></span>

<span data-ttu-id="4216a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4216a-113">S_OK</span></span> 
  
> <span data-ttu-id="4216a-114">A notificação foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="4216a-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4216a-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4216a-115">Remarks</span></span>

<span data-ttu-id="4216a-116">O processo de notificação começa quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para registrar-se para receber uma notificação de um tipo específico de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="4216a-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="4216a-117">Um dos parâmetros para o método **Advise** é um ponteiro para um objeto de coletor de eventos advise que implementa a interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4216a-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="4216a-118">Quando um evento ocorre ao objeto de destino que corresponde à notificação registrada, o provedor de serviço, direta ou indiretamente por meio de MAPI, chama o método de **OnNotify** do coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="4216a-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="4216a-119">A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4216a-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="4216a-120">Nos sistemas que oferecem suporte a vários threads de execução, **OnNotify** pode ser chamado no mesmo thread que foi usado para registro ou em um segmento diferente.</span><span class="sxs-lookup"><span data-stu-id="4216a-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="4216a-121">Os clientes podem Certifique-se de que a chamada **OnNotify** é feita no mesmo thread usado para chamar **Advise** criando o coletor de eventos advise que eles passam para **Advise** com a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="4216a-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="4216a-122">O parâmetro _lpNotifications_ aponta para uma ou mais estruturas de **notificação** que descrevem o que mudou durante o evento.</span><span class="sxs-lookup"><span data-stu-id="4216a-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="4216a-123">Há um tipo diferente de estrutura de **notificação** para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="4216a-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="4216a-124">A tabela a seguir lista os valores que são usados para representar os tipos possíveis de eventos e as estruturas associadas a cada valor:</span><span class="sxs-lookup"><span data-stu-id="4216a-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="4216a-125">**Tipo de evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="4216a-125">**Notification event type**</span></span>|<span data-ttu-id="4216a-126">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="4216a-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4216a-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="4216a-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="4216a-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4216a-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="4216a-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="4216a-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="4216a-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="4216a-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="4216a-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4216a-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="4216a-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="4216a-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4216a-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="4216a-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="4216a-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4216a-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="4216a-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="4216a-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4216a-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="4216a-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="4216a-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4216a-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="4216a-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="4216a-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="4216a-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="4216a-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="4216a-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="4216a-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="4216a-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="4216a-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4216a-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="4216a-147">Para obter mais informações sobre como configurar e interromper notificações, consulte as entradas de referência para os métodos **Advise** e **Unadvise** para qualquer uma das seguintes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="4216a-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="4216a-148">Para obter informações gerais sobre o processo de notificação, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4216a-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4216a-149">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="4216a-149">Notes to implementers</span></span>

<span data-ttu-id="4216a-150">A implementação de **OnNotify** consistirá normalmente um ou mais blocos de código para cada tipo de notificação que você espera receber.</span><span class="sxs-lookup"><span data-stu-id="4216a-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="4216a-151">Dentro desses blocos de código, execute qualquer tarefa que você considere necessário como uma resposta à notificação.</span><span class="sxs-lookup"><span data-stu-id="4216a-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="4216a-152">Por exemplo, suponha que você registre-se para receber notificações de **fnevObjectModified** em uma pasta que está incluído em uma exibição da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4216a-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="4216a-153">No bloco de código que você incluir no seu método **OnNotify** para manipular notificações de **fnevObjectModified** , você pode enviar uma mensagem de Windows à caixa de diálogo para solicitar um vídeo atualizado.</span><span class="sxs-lookup"><span data-stu-id="4216a-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="4216a-154">Não modifique ou livre a estrutura de **notificação** passada para **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="4216a-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="4216a-155">Os dados na estrutura são válidos somente até **OnNotify** retorna.</span><span class="sxs-lookup"><span data-stu-id="4216a-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4216a-156">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4216a-156">Notes to callers</span></span>

<span data-ttu-id="4216a-157">Quando ocorrem alterações a vários objetos, você pode notificar um coletor de advise registrados em uma única chamada de **OnNotify** ou em várias chamadas dependendo restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="4216a-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="4216a-158">Isso ocorre mesmo se as alterações são o resultado da chamada de um método ou várias.</span><span class="sxs-lookup"><span data-stu-id="4216a-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="4216a-159">Por exemplo, uma chamada para [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="4216a-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="4216a-160">Como um provedor de armazenamento de mensagem, você pode fazer uma chamada de **OnNotify** com um tipo de evento **fnevObjectModified** para a pasta de destino ou o número de chamadas, um para cada mensagens afetam.</span><span class="sxs-lookup"><span data-stu-id="4216a-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="4216a-161">Da mesma forma, se um cliente faz chamadas repetidas para [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), essas chamadas podem ser combinadas em um evento **fnevObjectModified** para a pasta ou separadas em individuais **fnevObjectCreated** eventos para cada nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="4216a-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="4216a-162">Para obter mais informações sobre como e quando gerar notificações, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md) e [Suporte a notificação de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="4216a-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4216a-163">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4216a-163">MFCMAPI reference</span></span>

<span data-ttu-id="4216a-164">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4216a-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4216a-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4216a-165">**File**</span></span>|<span data-ttu-id="4216a-166">**Function**</span><span class="sxs-lookup"><span data-stu-id="4216a-166">**Function**</span></span>|<span data-ttu-id="4216a-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4216a-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4216a-168">AdviseSink.h e AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="4216a-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="4216a-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="4216a-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="4216a-170">A classe CAdviseSink é implementada para lidar com todas as notificações de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="4216a-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4216a-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="4216a-171">See also</span></span>



[<span data-ttu-id="4216a-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4216a-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="4216a-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4216a-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4216a-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="4216a-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="4216a-175">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="4216a-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4216a-176">IMAPIAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4216a-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="4216a-177">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4216a-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

