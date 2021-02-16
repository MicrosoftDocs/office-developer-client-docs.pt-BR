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
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406273"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="b25db-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="b25db-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="b25db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b25db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b25db-105">Registra um cliente ou provedor de serviços para receber notificações sobre alterações em uma ou mais entradas no livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="b25db-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b25db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b25db-106">Parameters</span></span>

 <span data-ttu-id="b25db-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b25db-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b25db-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="b25db-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b25db-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b25db-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b25db-110">[in] Um ponteiro para o identificador de entrada do contêiner do address book, do usuário de mensagens ou da lista de distribuição que gerará uma notificação quando ocorrer uma alteração do tipo ou dos tipos descritos no _parâmetro ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="b25db-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="b25db-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="b25db-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="b25db-112">[in] Um ou mais eventos de notificação que o chamador está se registrando para receber.</span><span class="sxs-lookup"><span data-stu-id="b25db-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="b25db-113">Cada evento é associado a uma estrutura de notificação específica que contém informações sobre a alteração que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b25db-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="b25db-114">A tabela a seguir lista os valores válidos para  _ulEventMask_ e suas estruturas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b25db-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="b25db-115">**Evento de notificação**</span><span class="sxs-lookup"><span data-stu-id="b25db-115">**Notification event**</span></span>|<span data-ttu-id="b25db-116">**Estrutura correspondente**</span><span class="sxs-lookup"><span data-stu-id="b25db-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b25db-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="b25db-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="b25db-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="b25db-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="b25db-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="b25db-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b25db-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="b25db-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="b25db-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b25db-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="b25db-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="b25db-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b25db-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="b25db-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="b25db-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b25db-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="b25db-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="b25db-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b25db-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="b25db-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="b25db-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b25db-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="b25db-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="b25db-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="b25db-132">[in] Um ponteiro para o objeto sink de aviso a ser chamado quando o evento para o qual a notificação foi solicitada ocorre.</span><span class="sxs-lookup"><span data-stu-id="b25db-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="b25db-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="b25db-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="b25db-134">[out] Um ponteiro para um número de conexão que não seja zero que representa o registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="b25db-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b25db-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b25db-135">Return value</span></span>

<span data-ttu-id="b25db-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="b25db-136">S_OK</span></span> 
  
> <span data-ttu-id="b25db-137">O registro de notificação foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b25db-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="b25db-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b25db-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="b25db-139">O provedor de agendamento responsável pelo identificador de entrada passado  _em lpEntryID_ não pôde registrar uma notificação para a entrada correspondente.</span><span class="sxs-lookup"><span data-stu-id="b25db-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="b25db-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b25db-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b25db-141">A notificação não é suportada pelo provedor de agendas responsável pelo objeto identificador de entrada passado no _parâmetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="b25db-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b25db-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b25db-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b25db-143">O identificador de entrada passado  _em lpEntryID_ não pode ser manipulado por nenhum dos provedores de agendas no perfil.</span><span class="sxs-lookup"><span data-stu-id="b25db-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b25db-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b25db-144">Remarks</span></span>

<span data-ttu-id="b25db-145">Os clientes e provedores de serviços chamam o **método Advise** para se registrar para um tipo específico ou tipos de notificação em uma entrada do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="b25db-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="b25db-146">Os tipos de notificação são indicados pela máscara de evento passada com o _parâmetro ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="b25db-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="b25db-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="b25db-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="b25db-148">O provedor de agendamento de endereço trata o registro em si ou chama o método de suporte, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para solicitar MAPI para registrar o chamador.</span><span class="sxs-lookup"><span data-stu-id="b25db-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="b25db-149">Um número de conexão que não seja zero é retornado para representar o registro bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b25db-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="b25db-150">Sempre que ocorre uma alteração na entrada do tipo indicado pelo registro de notificação, o provedor de agendamento chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto sink de aviso especificado no parâmetro _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="b25db-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="b25db-151">O **método OnNotify** inclui uma estrutura [NOTIFICATION](notification.md) como um parâmetro de entrada que contém dados para descrever o evento.</span><span class="sxs-lookup"><span data-stu-id="b25db-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="b25db-152">Dependendo do provedor de agendamento de endereços, a chamada para **OnNotify** pode ocorrer imediatamente após a alteração no objeto registrado ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b25db-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="b25db-153">Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="b25db-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="b25db-154">Os clientes podem solicitar que essas notificações ocorram em um thread específico chamando a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar o objeto de evento de aviso que é passado para **Advise**.</span><span class="sxs-lookup"><span data-stu-id="b25db-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="b25db-155">Como um provedor de livro de endereços pode liberar o objeto de  evento de aviso passado pelos clientes a qualquer momento após a conclusão bem-sucedida  da chamada advise e antes de uma chamada [IAddrBook::Unadvise](iaddrbook-unadvise.md) para cancelar a notificação, os clientes devem liberar seus objetos de evento de aviso quando Advise retorna.</span><span class="sxs-lookup"><span data-stu-id="b25db-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="b25db-156">Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b25db-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b25db-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b25db-157">See also</span></span>



[<span data-ttu-id="b25db-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b25db-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="b25db-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b25db-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="b25db-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b25db-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b25db-161">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="b25db-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="b25db-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b25db-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

