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
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430228"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="ccbbe-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ccbbe-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="ccbbe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccbbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccbbe-105">Cancela o envio de notificações previamente configuradas com uma chamada para o método imApitable [:: Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="ccbbe-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ccbbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccbbe-106">Parameters</span></span>

 <span data-ttu-id="ccbbe-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ccbbe-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ccbbe-108">no O número da conexão de registro retornada por uma chamada para [IMAPITable:: Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="ccbbe-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccbbe-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ccbbe-109">Return value</span></span>

<span data-ttu-id="ccbbe-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccbbe-110">S_OK</span></span> 
  
> <span data-ttu-id="ccbbe-111">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccbbe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccbbe-112">Remarks</span></span>

<span data-ttu-id="ccbbe-113">Use o método imApitable **:: Unadvise** para liberar o ponteiro para o objeto de coletor de aviso passado no parâmetro _lpAdviseSink_ na chamada anterior a IMAPITable **:: Advise**, cancelando um registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="ccbbe-114">Como parte de descartar o ponteiro para o objeto de coletor de aviso, o método **IUnknown:: Release** do objeto é chamado.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="ccbbe-115">Geralmente, o **lançamento** é chamado durante a chamada de **Unadvise** , mas, se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o coletor de aviso, a chamada de **versão** será atrasada até que OnNotify \*\*\*\* método retorna.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="ccbbe-116">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ccbbe-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ccbbe-117">Para obter informações específicas sobre a notificação de tabela, consulte [about Table Notifications](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ccbbe-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ccbbe-118">Para obter informações sobre como usar os métodos **IMAPISupport** para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ccbbe-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccbbe-119">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ccbbe-119">MFCMAPI reference</span></span>

<span data-ttu-id="ccbbe-120">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccbbe-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ccbbe-121">**File**</span></span>|<span data-ttu-id="ccbbe-122">**Função**</span><span class="sxs-lookup"><span data-stu-id="ccbbe-122">**Function**</span></span>|<span data-ttu-id="ccbbe-123">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ccbbe-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccbbe-124">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="ccbbe-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ccbbe-125">CContentsTableListCtrl:: NotificationOff</span><span class="sxs-lookup"><span data-stu-id="ccbbe-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="ccbbe-126">MFCMAPI usa o método imApitable **:: Unadvise** para cancelar as notificações para a tabela.</span><span class="sxs-lookup"><span data-stu-id="ccbbe-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccbbe-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccbbe-127">See also</span></span>



[<span data-ttu-id="ccbbe-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ccbbe-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ccbbe-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ccbbe-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="ccbbe-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccbbe-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ccbbe-131">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ccbbe-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

