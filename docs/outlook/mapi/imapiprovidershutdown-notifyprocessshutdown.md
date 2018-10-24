---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592049"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="d0c5f-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="d0c5f-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="d0c5f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0c5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0c5f-105">Indica o provedor MAPI que um cliente MAPI irá fazer um rápido desligamento, para que o provedor pode executar ações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="d0c5f-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="d0c5f-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d0c5f-106">Return value</span></span>

<span data-ttu-id="d0c5f-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0c5f-107">S_OK</span></span>
  
> <span data-ttu-id="d0c5f-108">O provedor MAPI está demorando ações para evitar a perda de dados quando o cliente MAPI desligado.</span><span class="sxs-lookup"><span data-stu-id="d0c5f-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0c5f-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0c5f-109">See also</span></span>



[<span data-ttu-id="d0c5f-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0c5f-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="d0c5f-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c5f-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

