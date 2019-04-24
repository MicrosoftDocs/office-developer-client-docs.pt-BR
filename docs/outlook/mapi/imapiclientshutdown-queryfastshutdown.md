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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350866"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="b0bdc-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="b0bdc-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="b0bdc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0bdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0bdc-105">Consulta o subsistema MAPI para obter suporte de desligamento rápido fornecido por provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="b0bdc-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0bdc-106">Return value</span></span>

<span data-ttu-id="b0bdc-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0bdc-107">S_OK</span></span>
  
> <span data-ttu-id="b0bdc-108">O subsistema MAPI oferece suporte ao cliente MAPI para fazer desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="b0bdc-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b0bdc-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="b0bdc-110">O provedor MAPI não dá suporte ao cliente MAPI para fazer desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0bdc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0bdc-111">Remarks</span></span>

<span data-ttu-id="b0bdc-112">Se o subsistema MAPI suporta o cliente MAPI para fazer o desligamento rápido depende da configuração do registro do Windows do usuário ou o comportamento padrão do cliente MAPI para o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="b0bdc-113">Também depende da capacidade dos provedores MAPI carregados suportar o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="b0bdc-114">Para obter mais informações, consulte [Opções de usuário](fast-shutdown-user-options.md)de desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="b0bdc-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0bdc-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0bdc-115">See also</span></span>



[<span data-ttu-id="b0bdc-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0bdc-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="b0bdc-117">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="b0bdc-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

