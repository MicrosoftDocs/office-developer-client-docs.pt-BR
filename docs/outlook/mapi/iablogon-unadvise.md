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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424074"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="de0bd-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="de0bd-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="de0bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de0bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de0bd-105">Cancela as notificações que foram configuradas anteriormente com uma chamada para o método [IABLogon:: Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="de0bd-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="de0bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de0bd-106">Parameters</span></span>

 <span data-ttu-id="de0bd-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="de0bd-107">_ulConnection_</span></span>
  
> <span data-ttu-id="de0bd-108">no O número de conexão associado a um registro de notificação ativo.</span><span class="sxs-lookup"><span data-stu-id="de0bd-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="de0bd-109">Uma chamada anterior para **Advise** deve ter retornado o valor de _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="de0bd-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de0bd-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="de0bd-110">Return value</span></span>

<span data-ttu-id="de0bd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="de0bd-111">S_OK</span></span> 
  
> <span data-ttu-id="de0bd-112">O registro de notificação foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="de0bd-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de0bd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="de0bd-113">Remarks</span></span>

<span data-ttu-id="de0bd-114">MAPI chama o método **Unadvise** para cancelar um registro de notificação para um contêiner, usuário de mensagens ou objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="de0bd-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="de0bd-115">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="de0bd-115">Notes to implementers</span></span>

<span data-ttu-id="de0bd-116">A implementação de **Unadvise** dependerá se você dá suporte à notificação com a ajuda do MAPI ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="de0bd-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="de0bd-117">Se o MAPI fornecer seu suporte, chame o método [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="de0bd-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="de0bd-118">Se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de aviso, ele poderá ser adiado \*\*\*\* até que OnNotify tenha sido retornado.</span><span class="sxs-lookup"><span data-stu-id="de0bd-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="de0bd-119">Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="de0bd-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="de0bd-120">Para obter informações sobre como usar os métodos [IMAPISupport: IUnknown](imapisupportiunknown.md) para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="de0bd-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de0bd-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="de0bd-121">See also</span></span>



[<span data-ttu-id="de0bd-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="de0bd-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="de0bd-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="de0bd-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="de0bd-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de0bd-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

