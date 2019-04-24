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
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326387"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="6e446-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="6e446-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="6e446-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e446-105">Indica ao provedor MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa realizar ações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="6e446-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="6e446-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e446-106">Return value</span></span>

<span data-ttu-id="6e446-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e446-107">S_OK</span></span>
  
> <span data-ttu-id="6e446-108">O provedor MAPI está executando ações para evitar a perda de dados quando o cliente MAPI é desligado.</span><span class="sxs-lookup"><span data-stu-id="6e446-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e446-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e446-109">See also</span></span>



[<span data-ttu-id="6e446-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e446-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="6e446-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="6e446-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

