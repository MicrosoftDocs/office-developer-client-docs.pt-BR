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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766936"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="e9093-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="e9093-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="e9093-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9093-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9093-105">Indica a intenção do cliente MAPI para sair do processo de cliente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e9093-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="e9093-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e9093-106">Return value</span></span>

<span data-ttu-id="e9093-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9093-107">S_OK</span></span>
  
> <span data-ttu-id="e9093-108">O subsistema de MAPI tenha indicado para provedores MAPI carregados que o cliente MAPI está deixando imediatamente e os provedores MAPI estão prontos para sair do cliente.</span><span class="sxs-lookup"><span data-stu-id="e9093-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="e9093-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e9093-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="e9093-110">O subsistema de MAPI não suporta o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="e9093-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9093-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e9093-111">Remarks</span></span>

<span data-ttu-id="e9093-112">Para evitar a perda de dados do fast desligamento de um cliente MAPI, clientes MAPI devem chamar os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::DoFastShutdown** com base no resultado S_OK retornado pelo subsistema de MAPI em o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="e9093-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="e9093-113">Para obter mais informações, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="e9093-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9093-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9093-114">See also</span></span>



[<span data-ttu-id="e9093-115">IMAPIClientShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9093-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="e9093-116">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="e9093-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

