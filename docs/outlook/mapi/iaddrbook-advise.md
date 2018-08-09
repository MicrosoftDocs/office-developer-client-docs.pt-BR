---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766866"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="b0c4c-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="b0c4c-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="b0c4c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0c4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0c4c-105">Registra um provedor de serviço ou cliente para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b0c4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0c4c-106">Parameters</span></span>

 <span data-ttu-id="b0c4c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b0c4c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b0c4c-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b0c4c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b0c4c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b0c4c-110">[in] Um ponteiro para o identificador de entrada do recipiente de catálogo de endereços, usuário ou lista de distribuição que irá gerar uma notificação quando ocorre uma alteração do tipo ou tipos descritos no parâmetro _ulEventMask_ de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="b0c4c-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="b0c4c-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="b0c4c-112">[in] Um ou mais eventos de notificação que o chamador está registrando para receber.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="b0c4c-113">Cada evento é associado uma estrutura de notificação em particular que contém informações sobre a alteração que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="b0c4c-114">A tabela a seguir lista os valores válidos para _ulEventMask_ e suas estruturas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="b0c4c-115">**Evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-115">**Notification event**</span></span>|<span data-ttu-id="b0c4c-116">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0c4c-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="b0c4c-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="b0c4c-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="b0c4c-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b0c4c-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="b0c4c-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b0c4c-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="b0c4c-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b0c4c-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="b0c4c-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b0c4c-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="b0c4c-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b0c4c-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="b0c4c-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="b0c4c-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b0c4c-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="b0c4c-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="b0c4c-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="b0c4c-132">[in] Um ponteiro para o objeto coletor de eventos de advise a ser chamado quando ocorre o evento para o qual a notificação tiver sido solicitada.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="b0c4c-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="b0c4c-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="b0c4c-134">[out] Um ponteiro para um número diferente de zero de conexão que representa o registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0c4c-135">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b0c4c-135">Return value</span></span>

<span data-ttu-id="b0c4c-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0c4c-136">S_OK</span></span> 
  
> <span data-ttu-id="b0c4c-137">O registro de notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="b0c4c-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b0c4c-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="b0c4c-139">O provedor de catálogo de endereços para o identificador de entrada passado _lpEntryID_ responsável não pôde registrar uma notificação para a entrada correspondente.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="b0c4c-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b0c4c-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b0c4c-141">Notificação não é suportada pelo provedor de catálogo de endereços responsável pelo objeto identificado pelo identificador de entrada passado no parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b0c4c-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b0c4c-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b0c4c-143">O identificador de entrada passado _lpEntryID_ não pode ser manipulado por qualquer um dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b0c4c-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0c4c-144">Remarks</span></span>

<span data-ttu-id="b0c4c-145">Provedores de serviços e clientes chame o método de **Advise** para se registrar em um determinado tipo ou tipos de notificação em uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="b0c4c-146">Os tipos de notificação são indicados pela máscara de evento passada com o parâmetro _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="b0c4c-147">MAPI encaminha essa chamada **Advise** para o provedor de catálogo de endereços que é responsável pela entrada, conforme indicado pelo identificador de entrada no parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="b0c4c-148">O provedor de catálogo de endereços manipula o registro em si ou chama o método de suporte, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para solicitar o MAPI para registrar o chamador.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="b0c4c-149">Um número diferente de zero conexão é retornado para representar o registro com êxito.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="b0c4c-150">Sempre que ocorre uma alteração para a entrada do tipo indicado pelo registro notificação, o provedor de catálogo de endereços chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise especificado no parâmetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="b0c4c-151">O método **OnNotify** inclui uma estrutura de [notificação](notification.md) como um parâmetro de entrada que contém dados para descrever o evento.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="b0c4c-152">Dependendo do provedor de catálogo de endereços, a chamada para **OnNotify** pode ocorrer imediatamente após a alteração no objeto registrados ou mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="b0c4c-153">Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="b0c4c-154">Os clientes podem requisitar que essas notificações ocorrerem em um determinado thread chamando a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar o objeto de coletor de eventos de advise é passado para **Advise**.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="b0c4c-155">Porque um fornecedor de catálogo de endereços pode liberar o objeto coletor de eventos de advise passado pelos clientes a qualquer momento após a conclusão bem-sucedida do **Advise** e um [IAddrBook::Unadvise](iaddrbook-unadvise.md) antes de chamar para cancelar a notificação, clientes devem liberar seus objetos de coletor advise quando **Advise** retorna.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="b0c4c-156">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b0c4c-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0c4c-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0c4c-157">See also</span></span>



[<span data-ttu-id="b0c4c-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b0c4c-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="b0c4c-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b0c4c-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="b0c4c-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b0c4c-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b0c4c-161">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="b0c4c-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="b0c4c-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b0c4c-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

