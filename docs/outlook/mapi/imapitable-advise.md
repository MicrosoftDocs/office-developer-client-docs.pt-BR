---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329011"
---
# <a name="imapitableadvise"></a><span data-ttu-id="fabd6-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="fabd6-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="fabd6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fabd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fabd6-105">Registra um objeto de coletor de aviso para receber notificações de eventos especificados que afetam a tabela.</span><span class="sxs-lookup"><span data-stu-id="fabd6-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="fabd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fabd6-106">Parameters</span></span>

 <span data-ttu-id="fabd6-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="fabd6-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="fabd6-108">no O valor que indica o tipo de evento que gerará a notificação.</span><span class="sxs-lookup"><span data-stu-id="fabd6-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="fabd6-109">Apenas o seguinte valor é válido:</span><span class="sxs-lookup"><span data-stu-id="fabd6-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="fabd6-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="fabd6-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="fabd6-111">no Ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fabd6-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="fabd6-112">Este objeto de coletor de aviso deve já ter sido alocado.</span><span class="sxs-lookup"><span data-stu-id="fabd6-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="fabd6-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="fabd6-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="fabd6-114">bota Ponteiro para um valor diferente de zero que representa o registro de notificação bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fabd6-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fabd6-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fabd6-115">Return value</span></span>

<span data-ttu-id="fabd6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fabd6-116">S_OK</span></span> 
  
> <span data-ttu-id="fabd6-117">O registro de notificação foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="fabd6-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="fabd6-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fabd6-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="fabd6-119">A implementação de tabela não oferece suporte a alterações em suas linhas e colunas ou não oferece suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="fabd6-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fabd6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fabd6-120">Remarks</span></span>

<span data-ttu-id="fabd6-121">Use o método imApitable **:: Advise** para registrar um objeto Table implementado no provedor para retornos de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="fabd6-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="fabd6-122">Sempre que uma alteração ocorre no objeto Table, o provedor verifica se o bit de máscara de evento foi definido no parâmetro _ulEventMask_ e, portanto, que tipo de alteração ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fabd6-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="fabd6-123">Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o objeto de coletor de aviso indicado pelo parâmetro _lpAdviseSink_ para relatar o evento.</span><span class="sxs-lookup"><span data-stu-id="fabd6-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="fabd6-124">Dados passados na estrutura de notificação para a \*\*\*\* rotina OnNotify descreve o evento.</span><span class="sxs-lookup"><span data-stu-id="fabd6-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="fabd6-125">A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou no momento seguinte.</span><span class="sxs-lookup"><span data-stu-id="fabd6-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="fabd6-126">Em sistemas que oferecem suporte a vários threads de execução, \*\*\*\* a chamada para OnNotify pode ocorrer em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="fabd6-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="fabd6-127">Para obter uma chamada para onNotificar \*\*\*\* que pode ocorrer em um horário do inopportune em um que seja mais seguro para lidar, um provedor deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="fabd6-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="fabd6-128">Para fornecer notificações, a **recomendação** de provedor de implementação precisa manter uma cópia do ponteiro para o objeto do coletor de aviso _lpAdviseSink_ ; para fazer isso, ele chama o método **IUnknown:: AddRef** para o coletor de avisos para manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método IMAPITable [:: Unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="fabd6-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="fabd6-129">A implementação de **aviso** deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de devolvê-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="fabd6-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="fabd6-130">Os provedores de serviços podem liberar o objeto de coletor de aviso antes de o registro ser cancelado, mas não devem liberar o número de conexão até que \* \* Unadvise \* \* tenha sido chamado.</span><span class="sxs-lookup"><span data-stu-id="fabd6-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="fabd6-131">Após uma chamada a **Advise** ter sido bem-sucedida e antes de \* \* Unadvise \* \* ter sido chamado, os clientes devem estar preparados para que o objeto de coletor de aviso seja liberado.</span><span class="sxs-lookup"><span data-stu-id="fabd6-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="fabd6-132">No entanto, um cliente deve liberar seu objeto \*\*\*\* de coletor de aviso após a revisor, a menos que tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="fabd6-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="fabd6-133">Devido ao comportamento assíncrono da notificação, as implementações que alteram as configurações de coluna da tabela podem receber notificações com informações organizadas em uma ordem de coluna anterior.</span><span class="sxs-lookup"><span data-stu-id="fabd6-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="fabd6-134">Por exemplo, uma linha de tabela pode ser retornada para uma mensagem que acabou de ser excluída do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fabd6-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="fabd6-135">Tal notificação é enviada quando a alteração da configuração da coluna tiver sido feita e informações sobre ela enviadas, mas a exibição da tabela de notificação ainda não tiver sido atualizada com essas informações.</span><span class="sxs-lookup"><span data-stu-id="fabd6-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="fabd6-136">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="fabd6-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="fabd6-137">Para obter informações específicas sobre a notificação de tabela, consulte [about Table Notifications](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fabd6-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="fabd6-138">Para obter informações sobre como usar os métodos **IMAPISupport** para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="fabd6-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fabd6-139">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fabd6-139">MFCMAPI reference</span></span>

<span data-ttu-id="fabd6-140">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fabd6-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fabd6-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fabd6-141">**File**</span></span>|<span data-ttu-id="fabd6-142">**Função**</span><span class="sxs-lookup"><span data-stu-id="fabd6-142">**Function**</span></span>|<span data-ttu-id="fabd6-143">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="fabd6-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fabd6-144">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="fabd6-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fabd6-145">CContestTableListCtrl:: notificação</span><span class="sxs-lookup"><span data-stu-id="fabd6-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="fabd6-146">MFCMAPI usa o método imApitable **:: Advise** para registrar notificações para permitir que o modo de exibição de tabela permaneça atualizado.</span><span class="sxs-lookup"><span data-stu-id="fabd6-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fabd6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="fabd6-147">See also</span></span>



[<span data-ttu-id="fabd6-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="fabd6-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="fabd6-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="fabd6-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="fabd6-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fabd6-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="fabd6-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="fabd6-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="fabd6-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fabd6-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="fabd6-153">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fabd6-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

