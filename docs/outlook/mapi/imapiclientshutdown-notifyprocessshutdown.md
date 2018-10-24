---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568263"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="1bb1a-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="1bb1a-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="1bb1a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bb1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bb1a-105">Indica a intenção do cliente MAPI para prosseguir com desligado.</span><span class="sxs-lookup"><span data-stu-id="1bb1a-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="1bb1a-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1bb1a-106">Return value</span></span>

<span data-ttu-id="1bb1a-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bb1a-107">S_OK</span></span>
  
> <span data-ttu-id="1bb1a-108">O subsistema de MAPI tentou notificar carregados provedores MAPI que o cliente MAPI irá fazer um desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="1bb1a-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bb1a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bb1a-109">Remarks</span></span>

<span data-ttu-id="1bb1a-110">Para evitar a perda de dados do fast desligamento de um cliente MAPI, clientes MAPI devem chamar os métodos **IMAPIClientShutdown::NotifyProcessShutdown** e [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) com base no resultado S_OK retornado pelo subsistema de MAPI em o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb1a-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="1bb1a-111">Para obter mais informações, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="1bb1a-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1bb1a-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bb1a-112">See also</span></span>



[<span data-ttu-id="1bb1a-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bb1a-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="1bb1a-114">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb1a-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

