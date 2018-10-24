---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567885"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="bfb60-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="bfb60-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="bfb60-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfb60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfb60-105">Cancela uma conexão para uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="bfb60-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bfb60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfb60-106">Parameters</span></span>

 <span data-ttu-id="bfb60-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="bfb60-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="bfb60-108">[In] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="bfb60-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfb60-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bfb60-109">Return value</span></span>

<span data-ttu-id="bfb60-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfb60-110">S_OK</span></span> 
  
> <span data-ttu-id="bfb60-111">A conexão foi cancelada com êxito.</span><span class="sxs-lookup"><span data-stu-id="bfb60-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="bfb60-112">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="bfb60-112">Notes to implementers</span></span>

<span data-ttu-id="bfb60-113">Em sua implementação do método **desligamento** , execute as tarefas que você considerar necessário.</span><span class="sxs-lookup"><span data-stu-id="bfb60-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="bfb60-114">MAPI chama seu método de **desligamento** somente depois de você ter lançado todos os seus objetos de logon.</span><span class="sxs-lookup"><span data-stu-id="bfb60-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bfb60-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfb60-115">See also</span></span>



[<span data-ttu-id="bfb60-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bfb60-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

