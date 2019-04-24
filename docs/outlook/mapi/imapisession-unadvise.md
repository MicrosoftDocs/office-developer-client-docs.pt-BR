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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335697"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="332b2-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="332b2-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="332b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="332b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="332b2-105">Cancela o envio de notificações anteriormente configuradas com uma chamada para o método [IMAPISession:: Advise](imapisession-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="332b2-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="332b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="332b2-106">Parameters</span></span>

 <span data-ttu-id="332b2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="332b2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="332b2-108">no Um número de conexão associado a um registro de notificação ativo.</span><span class="sxs-lookup"><span data-stu-id="332b2-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="332b2-109">O valor de _ulConnection_ deve ter sido retornado por uma chamada anterior para **IMAPISession:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="332b2-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="332b2-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="332b2-110">Return value</span></span>

<span data-ttu-id="332b2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="332b2-111">S_OK</span></span> 
  
> <span data-ttu-id="332b2-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="332b2-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="332b2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="332b2-113">Remarks</span></span>

<span data-ttu-id="332b2-114">O método **IMAPISession:: Unadvise** cancela um registro para notificação.</span><span class="sxs-lookup"><span data-stu-id="332b2-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="332b2-115">**Unadvise** libera seu ponteiro para o coletor de aviso do chamador, que ele recebeu na chamada de **aviso** usada para registro.</span><span class="sxs-lookup"><span data-stu-id="332b2-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="332b2-116">Em geral, **Unadvise** chama o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do coletor de aviso, durante a chamada de **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="332b2-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="332b2-117">No enTanto, se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de aviso, a chamada de **versão** será atrasada até o método OnNotify retornar. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="332b2-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="332b2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="332b2-118">See also</span></span>



[<span data-ttu-id="332b2-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="332b2-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="332b2-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="332b2-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="332b2-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="332b2-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

