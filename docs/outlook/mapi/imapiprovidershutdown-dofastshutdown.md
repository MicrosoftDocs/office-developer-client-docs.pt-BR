---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767146"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="ed11f-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ed11f-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="ed11f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed11f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed11f-105">Indica o provedor MAPI que o cliente MAPI está deixando imediatamente, para que o provedor MAPI persistirá alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="ed11f-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ed11f-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ed11f-106">Return value</span></span>

<span data-ttu-id="ed11f-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed11f-107">S_OK</span></span>
  
> <span data-ttu-id="ed11f-108">O provedor MAPI está pronto para o cliente MAPI sair imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ed11f-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ed11f-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed11f-109">See also</span></span>



[<span data-ttu-id="ed11f-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed11f-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="ed11f-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="ed11f-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

