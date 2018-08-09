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
ms.openlocfilehash: 781146193748cdd9408a3320e90a73a070ced2af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767327"
---
# <a name="imapitableadvise"></a><span data-ttu-id="d1ee7-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="d1ee7-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="d1ee7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1ee7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1ee7-105">Registra um objeto de coletor de eventos advise para receber notificações de eventos especificados que afetam a tabela.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d1ee7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1ee7-106">Parameters</span></span>

 <span data-ttu-id="d1ee7-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="d1ee7-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="d1ee7-108">[in] Valor que indica o tipo de evento que irá gerar a notificação.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="d1ee7-109">O seguinte valor só é válido:</span><span class="sxs-lookup"><span data-stu-id="d1ee7-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="d1ee7-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d1ee7-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="d1ee7-111">[in] Ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="d1ee7-112">Este objeto de coletor de eventos advise deve foram já alocado.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="d1ee7-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="d1ee7-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="d1ee7-114">[out] Ponteiro para um valor diferente de zero que representa o registro de notificação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1ee7-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d1ee7-115">Return value</span></span>

<span data-ttu-id="d1ee7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1ee7-116">S_OK</span></span> 
  
> <span data-ttu-id="d1ee7-117">O registro de notificação concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="d1ee7-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d1ee7-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d1ee7-119">A implementação de tabela não oferece suporte a alterações em suas linhas e colunas ou não oferece suporte a notificação.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1ee7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1ee7-120">Remarks</span></span>

<span data-ttu-id="d1ee7-121">Use o método **IMAPITable::Advise** para registrar um objeto table implementado no provedor para retornos de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="d1ee7-122">Sempre que ocorre uma alteração ao objeto table, o provedor verifica quais bits de máscara de evento foi definida no parâmetro _ulEventMask_ e, portanto, o tipo de alteração que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="d1ee7-123">Se um pouco for definido, o provedor chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise indicado pelo parâmetro _lpAdviseSink_ para relatar o evento.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="d1ee7-124">Dados passados na estrutura de notificação para a rotina de **OnNotify** descrevem o evento.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="d1ee7-125">A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="d1ee7-126">Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="d1ee7-127">Para ativar uma chamada para **OnNotify** que pode acontecer um inoportunos momento em que é mais seguro lidar com uma maneira, um provedor deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ee7-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="d1ee7-128">Para fornecer notificações, o provedor implementing **Advise** precisa manter uma cópia do ponteiro para o _lpAdviseSink_ avise o objeto coletor de eventos; Para fazer isso, ele chama o método **AddRef** para o coletor de eventos advise manter seu indicador de objeto até que o registro de notificação será cancelado com uma chamada ao método [IMAPITable::Unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ee7-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="d1ee7-129">A implementação de **Advise** deve atribuir um número de conexão para o registro de notificação e chamar **AddRef** este número de conexão antes de retorná-lo no parâmetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="d1ee7-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="d1ee7-130">Provedores de serviços podem liberar o objeto coletor de eventos advise antes que o registro será cancelado, mas eles não devem liberar o número de conexão até * * Unadvise * * foi chamado.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until ** Unadvise ** has been called.</span></span> 
  
<span data-ttu-id="d1ee7-131">Depois que uma chamada para **Advise** teve sucesso e antes * * Unadvise * * tenha sido chamado, os clientes devem ser preparados para o objeto coletor de eventos de advise ser liberada.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-131">After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="d1ee7-132">Um cliente, portanto, deve liberar seu objeto de coletor advise depois **Advise** retorna a menos que ele tenha um uso específico de longo prazo para ele.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="d1ee7-133">Devido ao comportamento assíncrono da notificação, implementações que alterar as configurações de coluna de tabela podem receber notificações com informações organizadas em uma ordem de coluna anterior.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="d1ee7-134">Por exemplo, uma linha da tabela pode ser retornada por uma mensagem que foi excluída do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="d1ee7-135">Tal uma notificação é enviada quando foi feita a alteração de configuração de coluna e informações sobre ele enviadas, mas o modo de exibição de tabela de notificação não foi atualizado com essas informações ainda.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="d1ee7-136">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d1ee7-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="d1ee7-137">Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d1ee7-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="d1ee7-138">Para obter informações sobre como usar os métodos **IMAPISupport** para suportar a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="d1ee7-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d1ee7-139">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d1ee7-139">MFCMAPI reference</span></span>

<span data-ttu-id="d1ee7-140">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d1ee7-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d1ee7-141">**File**</span></span>|<span data-ttu-id="d1ee7-142">**Function**</span><span class="sxs-lookup"><span data-stu-id="d1ee7-142">**Function**</span></span>|<span data-ttu-id="d1ee7-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d1ee7-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1ee7-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d1ee7-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d1ee7-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="d1ee7-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="d1ee7-146">MFCMAPI usa o método **IMAPITable::Advise** para registrar para notificações permitir que o modo de exibição de tabela permaneçam atual.</span><span class="sxs-lookup"><span data-stu-id="d1ee7-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1ee7-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1ee7-147">See also</span></span>



[<span data-ttu-id="d1ee7-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d1ee7-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="d1ee7-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d1ee7-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d1ee7-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="d1ee7-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="d1ee7-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d1ee7-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d1ee7-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1ee7-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d1ee7-153">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d1ee7-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

