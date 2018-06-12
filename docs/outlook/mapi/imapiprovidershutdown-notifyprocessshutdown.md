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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767167"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="02fb2-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="02fb2-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="02fb2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02fb2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02fb2-105">Indica o provedor MAPI que um cliente MAPI irá fazer um rápido desligamento, para que o provedor pode executar ações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="02fb2-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="02fb2-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="02fb2-106">Return value</span></span>

<span data-ttu-id="02fb2-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="02fb2-107">S_OK</span></span>
  
> <span data-ttu-id="02fb2-108">O provedor MAPI está demorando ações para evitar a perda de dados quando o cliente MAPI desligado.</span><span class="sxs-lookup"><span data-stu-id="02fb2-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02fb2-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="02fb2-109">See also</span></span>



[<span data-ttu-id="02fb2-110">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="02fb2-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="02fb2-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="02fb2-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

