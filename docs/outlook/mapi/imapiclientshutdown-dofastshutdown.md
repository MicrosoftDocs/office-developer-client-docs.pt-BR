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
ms.openlocfilehash: 41c4ee65ce6ae8f2e0d978f1e2bd95adb4f5872a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575172"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="ad850-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ad850-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="ad850-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad850-105">Indica a intenção do cliente MAPI para sair do processo de cliente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ad850-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ad850-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad850-106">Return value</span></span>

<span data-ttu-id="ad850-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad850-107">S_OK</span></span>
  
> <span data-ttu-id="ad850-108">O subsistema de MAPI tenha indicado para provedores MAPI carregados que o cliente MAPI está deixando imediatamente e os provedores MAPI estão prontos para sair do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad850-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="ad850-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ad850-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="ad850-110">O subsistema de MAPI não suporta o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad850-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad850-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad850-111">Remarks</span></span>

<span data-ttu-id="ad850-112">Para evitar a perda de dados do fast desligamento de um cliente MAPI, clientes MAPI devem chamar os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::DoFastShutdown** com base no resultado S_OK retornado pelo subsistema de MAPI em o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="ad850-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="ad850-113">Para obter mais informações, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="ad850-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad850-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad850-114">See also</span></span>



[<span data-ttu-id="ad850-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad850-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="ad850-116">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="ad850-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

