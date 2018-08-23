---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584930"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="c28c4-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c28c4-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="c28c4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c28c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c28c4-105">O subsistema MAPI para desligamento rápido de consultas suporte que é fornecido por provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="c28c4-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="c28c4-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c28c4-106">Return value</span></span>

<span data-ttu-id="c28c4-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="c28c4-107">S_OK</span></span>
  
> <span data-ttu-id="c28c4-108">O subsistema de MAPI suporta o cliente MAPI para rápida desligamento.</span><span class="sxs-lookup"><span data-stu-id="c28c4-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="c28c4-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c28c4-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="c28c4-110">O provedor MAPI não suporta o cliente MAPI para rápida desligamento.</span><span class="sxs-lookup"><span data-stu-id="c28c4-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c28c4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c28c4-111">Remarks</span></span>

<span data-ttu-id="c28c4-112">Se o subsistema de MAPI suporta o cliente MAPI rápida desligamento depende da configuração de registro do Windows do usuário ou o comportamento padrão do cliente MAPI para desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="c28c4-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="c28c4-113">Ele também depende da capacidade dos provedores MAPI carregados para suportar o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="c28c4-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="c28c4-114">Para obter mais informações, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="c28c4-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c28c4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c28c4-115">See also</span></span>



[<span data-ttu-id="c28c4-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c28c4-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="c28c4-117">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="c28c4-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

