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
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563468"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="8c501-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8c501-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="8c501-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c501-105">Indica o provedor MAPI que o cliente MAPI está deixando imediatamente, para que o provedor MAPI persistirá alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8c501-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="8c501-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8c501-106">Return value</span></span>

<span data-ttu-id="8c501-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c501-107">S_OK</span></span>
  
> <span data-ttu-id="8c501-108">O provedor MAPI está pronto para o cliente MAPI sair imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8c501-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8c501-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c501-109">See also</span></span>



[<span data-ttu-id="8c501-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c501-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="8c501-111">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="8c501-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

