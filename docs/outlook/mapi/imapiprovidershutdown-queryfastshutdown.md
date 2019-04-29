---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418215"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="8b546-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8b546-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="8b546-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b546-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b546-105">Consulta o provedor MAPI para obter suporte para desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="8b546-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="8b546-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8b546-106">Return value</span></span>

<span data-ttu-id="8b546-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b546-107">S_OK</span></span>
  
> <span data-ttu-id="8b546-108">O provedor MAPI dá suporte ao cliente MAPI para fazer desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="8b546-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="8b546-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8b546-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="8b546-110">O provedor MAPI não dá suporte ao cliente MAPI para fazer desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="8b546-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b546-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b546-111">Remarks</span></span>

<span data-ttu-id="8b546-112">Os provedores MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) e fazer com que o método **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** retorne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="8b546-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="8b546-113">Para o Outlook como um cliente MAPI, isso faz com que o Outlook espere que todas as referências externas sejam liberadas antes de sair.</span><span class="sxs-lookup"><span data-stu-id="8b546-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="8b546-114">Dependendo da configuração do registro do Windows do usuário para desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede um desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="8b546-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b546-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b546-115">See also</span></span>



[<span data-ttu-id="8b546-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b546-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="8b546-117">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="8b546-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

