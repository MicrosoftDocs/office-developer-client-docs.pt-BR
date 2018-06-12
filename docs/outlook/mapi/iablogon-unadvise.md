---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766848"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="42328-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="42328-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="42328-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42328-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42328-105">Cancela notificações que foram definidas com uma chamada ao método [IABLogon::Advise](iablogon-advise.md) anteriormente.</span><span class="sxs-lookup"><span data-stu-id="42328-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="42328-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="42328-106">Parameters</span></span>

 <span data-ttu-id="42328-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="42328-107">_ulConnection_</span></span>
  
> <span data-ttu-id="42328-108">[in] O número de conexão associado a um registro de notificação ativo.</span><span class="sxs-lookup"><span data-stu-id="42328-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="42328-109">Uma chamada anterior a **Advise** deve ter retornado o valor de _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="42328-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42328-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="42328-110">Return value</span></span>

<span data-ttu-id="42328-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="42328-111">S_OK</span></span> 
  
> <span data-ttu-id="42328-112">O registro de notificação foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="42328-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42328-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="42328-113">Remarks</span></span>

<span data-ttu-id="42328-114">MAPI chama o método **Unadvise** para cancelar um registro de notificação para um contêiner, usuário ou objeto de lista de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="42328-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="42328-115">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="42328-115">Notes to implementers</span></span>

<span data-ttu-id="42328-116">A implementação dos **Unadvise** dependerá se você oferecer suporte a notificação com a Ajuda do MAPI ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="42328-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="42328-117">Se MAPI fornece seu suporte, chame o método de [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="42328-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="42328-118">Se outro thread no processo de chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise, ela pode ser atrasada até **OnNotify** ter retornado.</span><span class="sxs-lookup"><span data-stu-id="42328-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="42328-119">Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="42328-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="42328-120">Para obter informações sobre como usar o [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos para dar suporte a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="42328-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42328-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="42328-121">See also</span></span>



[<span data-ttu-id="42328-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="42328-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="42328-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="42328-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="42328-124">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="42328-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

