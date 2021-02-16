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
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="63c92-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="63c92-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="63c92-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63c92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63c92-105">Indica a intenção do cliente MAPI de sair do processo de cliente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="63c92-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="63c92-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63c92-106">Return value</span></span>

<span data-ttu-id="63c92-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="63c92-107">S_OK</span></span>
  
> <span data-ttu-id="63c92-108">O subsistema de MAPI indicou para os provedores de MAPI carregados que o cliente MAPI está saindo imediatamente, e os provedores de MAPI estão prontos para a saída do cliente.</span><span class="sxs-lookup"><span data-stu-id="63c92-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="63c92-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="63c92-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="63c92-110">O subsistema MAPI não dá suporte ao desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="63c92-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63c92-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="63c92-111">Remarks</span></span>

<span data-ttu-id="63c92-112">Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::D oFastShutdown** com base no resultado S_OK retornado pelo subsistema de MAPI no método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="63c92-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="63c92-113">Para obter mais informações, consulte [As Práticas Recomendadas para o Desligamento Rápido.](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="63c92-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63c92-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="63c92-114">See also</span></span>



[<span data-ttu-id="63c92-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63c92-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="63c92-116">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="63c92-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

