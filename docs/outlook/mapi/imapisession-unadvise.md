---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 25f80ddce60ab5a8966a62761d234accafbb54be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767203"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="8dd7c-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8dd7c-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="8dd7c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8dd7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8dd7c-105">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método [IMAPISession::Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd7c-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8dd7c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8dd7c-106">Parameters</span></span>

 <span data-ttu-id="8dd7c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="8dd7c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="8dd7c-108">[in] Um número de conexão associado a um registro de notificação ativo.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="8dd7c-109">O valor de _ulConnection_ deve ter retornado por uma chamada anterior para **IMAPISession::Advise**.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8dd7c-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8dd7c-110">Return value</span></span>

<span data-ttu-id="8dd7c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dd7c-111">S_OK</span></span> 
  
> <span data-ttu-id="8dd7c-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8dd7c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dd7c-113">Remarks</span></span>

<span data-ttu-id="8dd7c-114">O método **IMAPISession::Unadvise** cancela um registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="8dd7c-115">Versões de **Unadvise** coletor, o que ele recebido na chamada **Advise** usada para o registro de aviso de seu ponteiro para o chamador.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="8dd7c-116">Geralmente, o **Unadvise** chama o método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) do coletor de eventos advise durante a chamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8dd7c-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="8dd7c-117">No entanto, se outro thread no processo de chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise, a chamada de **liberação** foi adiada até que o método **OnNotify** retorna.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8dd7c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dd7c-118">See also</span></span>



[<span data-ttu-id="8dd7c-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8dd7c-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8dd7c-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="8dd7c-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="8dd7c-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8dd7c-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

