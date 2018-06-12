---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 516de39d721c532c003775bd366a52ed8144ab88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767533"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="835e2-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="835e2-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="835e2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="835e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="835e2-105">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="835e2-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="835e2-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="835e2-106">Parameters</span></span>

 <span data-ttu-id="835e2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="835e2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="835e2-108">[in] O número de conexão associado a um registro de notificação ativo.</span><span class="sxs-lookup"><span data-stu-id="835e2-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="835e2-109">O valor de _ulConnection_ deve ter retornado por uma chamada anterior para o método **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="835e2-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="835e2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="835e2-110">Return value</span></span>

<span data-ttu-id="835e2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="835e2-111">S_OK</span></span> 
  
> <span data-ttu-id="835e2-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="835e2-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="835e2-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="835e2-113">Remarks</span></span>

<span data-ttu-id="835e2-114">O método **IMsgStore::Unadvise** cancela um registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="835e2-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="835e2-115">Versões de **Unadvise** coletor, o que ele recebido na chamada **Advise** usada para o registro de aviso de seu ponteiro para o chamador.</span><span class="sxs-lookup"><span data-stu-id="835e2-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="835e2-116">Geralmente, o **Unadvise** chama o método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) do coletor de eventos advise durante a chamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="835e2-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="835e2-117">No entanto, se outro thread no processo de chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise, a chamada de **liberação** foi adiada até que o método **OnNotify** retorna.</span><span class="sxs-lookup"><span data-stu-id="835e2-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="835e2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="835e2-118">See also</span></span>



[<span data-ttu-id="835e2-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="835e2-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="835e2-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="835e2-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="835e2-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="835e2-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

