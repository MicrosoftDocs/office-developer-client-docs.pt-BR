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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4301fb504439cf0ebd70b5ece589c812cb74844e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585294"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="e28ba-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="e28ba-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="e28ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28ba-105">Suporte a consultas o provedor MAPI para o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="e28ba-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="e28ba-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e28ba-106">Return value</span></span>

<span data-ttu-id="e28ba-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="e28ba-107">S_OK</span></span>
  
> <span data-ttu-id="e28ba-108">O provedor MAPI suporta o cliente MAPI para rápida desligamento.</span><span class="sxs-lookup"><span data-stu-id="e28ba-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="e28ba-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e28ba-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="e28ba-110">O provedor MAPI não suporta o cliente MAPI para rápida desligamento.</span><span class="sxs-lookup"><span data-stu-id="e28ba-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e28ba-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e28ba-111">Remarks</span></span>

<span data-ttu-id="e28ba-112">Provedores MAPI que não é necessário para suportar o desligamento rápido do cliente ainda devem implementar a interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) e têm o método **IMAPIProviderShutdown::QueryFastShutdown** retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="e28ba-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="e28ba-113">Para o Outlook como um cliente MAPI, isso faz com que o Outlook esperar por todas as referências externas ser liberada antes de sair.</span><span class="sxs-lookup"><span data-stu-id="e28ba-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="e28ba-114">Dependendo do registro do Windows do usuário configuração para fast desligamento, não Implementando a interface de **IMAPIProviderShutdown** não necessariamente impede que um desligamento rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="e28ba-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e28ba-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e28ba-115">See also</span></span>



[<span data-ttu-id="e28ba-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e28ba-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="e28ba-117">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="e28ba-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

