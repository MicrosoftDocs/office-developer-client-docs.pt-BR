---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408681"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="2128f-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="2128f-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="2128f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2128f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2128f-105">Indica a intenção de que o cliente MAPI saia imediatamente do processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="2128f-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="2128f-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2128f-106">Return value</span></span>

<span data-ttu-id="2128f-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="2128f-107">S_OK</span></span>
  
> <span data-ttu-id="2128f-108">O subsistema MAPI indicou que carregou provedores MAPI que o cliente MAPI está saindo imediatamente e os provedores MAPI estão prontos para a saída do cliente.</span><span class="sxs-lookup"><span data-stu-id="2128f-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="2128f-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2128f-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="2128f-110">O subsistema MAPI não dá suporte a desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="2128f-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2128f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2128f-111">Remarks</span></span>

<span data-ttu-id="2128f-112">Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::D ofastshutdown** com base no resultado de S_OK RETORNADO pelo subsistema MAPI no o método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="2128f-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="2128f-113">Para obter mais informações, consulte [práticas recomendadas para](best-practices-for-fast-shutdown.md)o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="2128f-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2128f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2128f-114">See also</span></span>



[<span data-ttu-id="2128f-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2128f-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="2128f-116">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="2128f-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

