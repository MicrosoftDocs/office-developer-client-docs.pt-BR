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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322418"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="32b1c-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="32b1c-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="32b1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32b1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32b1c-105">Indica ao provedor MAPI que o cliente MAPI está saindo imediatamente, para que o provedor MAPI persista as alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="32b1c-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="32b1c-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="32b1c-106">Return value</span></span>

<span data-ttu-id="32b1c-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="32b1c-107">S_OK</span></span>
  
> <span data-ttu-id="32b1c-108">O provedor MAPI está pronto para que o cliente MAPI saia imediatamente.</span><span class="sxs-lookup"><span data-stu-id="32b1c-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="32b1c-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="32b1c-109">See also</span></span>



[<span data-ttu-id="32b1c-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32b1c-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="32b1c-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="32b1c-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

