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
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438866"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="49ee0-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="49ee0-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="49ee0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49ee0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49ee0-105">Indica a intenção do cliente MAPI para prosseguir com o desligamento.</span><span class="sxs-lookup"><span data-stu-id="49ee0-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="49ee0-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="49ee0-106">Return value</span></span>

<span data-ttu-id="49ee0-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="49ee0-107">S_OK</span></span>
  
> <span data-ttu-id="49ee0-108">O subsistema MAPI tentou notificar os provedores MAPI carregados de que o cliente MAPI fará um desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="49ee0-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49ee0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="49ee0-109">Remarks</span></span>

<span data-ttu-id="49ee0-110">Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos **IMAPIClientShutdown:: NotifyProcessShutdown** e [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) com base no resultado de S_OK RETORNADO pelo subsistema MAPI no o método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="49ee0-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="49ee0-111">Para obter mais informações, consulte [práticas recomendadas para](best-practices-for-fast-shutdown.md)o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="49ee0-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49ee0-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="49ee0-112">See also</span></span>



[<span data-ttu-id="49ee0-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49ee0-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="49ee0-114">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="49ee0-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

