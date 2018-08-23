---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7de4d3c58d5eeefcf9a82235333da5db4703bc8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592973"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="5e82c-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5e82c-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="5e82c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e82c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e82c-105">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método [IMAPITable::Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="5e82c-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5e82c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5e82c-106">Parameters</span></span>

 <span data-ttu-id="5e82c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5e82c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5e82c-108">[in] O número da conexão de registro retornado por uma chamada para [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="5e82c-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e82c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5e82c-109">Return value</span></span>

<span data-ttu-id="5e82c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e82c-110">S_OK</span></span> 
  
> <span data-ttu-id="5e82c-111">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5e82c-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e82c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e82c-112">Remarks</span></span>

<span data-ttu-id="5e82c-113">Use o método **IMAPITable::Unadvise** para liberar o ponteiro para o objeto de coletor de eventos de advise passado no parâmetro _lpAdviseSink_ na chamada anterior a **IMAPITable::Advise**, assim, Cancelando um registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="5e82c-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="5e82c-114">Como parte do descartar o ponteiro para o objeto coletor de eventos advise, o método do objeto **IUnknown:: Release** é chamado.</span><span class="sxs-lookup"><span data-stu-id="5e82c-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="5e82c-115">Geralmente, a **versão** é chamado durante a chamada **Unadvise** , mas se outro thread está em processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o coletor de advise, a chamada de **liberação** foi adiada até o **OnNotify** método retorna.</span><span class="sxs-lookup"><span data-stu-id="5e82c-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="5e82c-116">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="5e82c-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="5e82c-117">Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5e82c-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="5e82c-118">Para obter informações sobre como usar os métodos **IMAPISupport** para suportar a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="5e82c-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e82c-119">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5e82c-119">MFCMAPI reference</span></span>

<span data-ttu-id="5e82c-120">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e82c-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e82c-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5e82c-121">**File**</span></span>|<span data-ttu-id="5e82c-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="5e82c-122">**Function**</span></span>|<span data-ttu-id="5e82c-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5e82c-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e82c-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5e82c-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5e82c-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="5e82c-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="5e82c-126">MFCMAPI usa o método **IMAPITable::Unadvise** para cancelar as notificações para a tabela.</span><span class="sxs-lookup"><span data-stu-id="5e82c-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e82c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e82c-127">See also</span></span>



[<span data-ttu-id="5e82c-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5e82c-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5e82c-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="5e82c-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="5e82c-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e82c-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5e82c-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5e82c-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

