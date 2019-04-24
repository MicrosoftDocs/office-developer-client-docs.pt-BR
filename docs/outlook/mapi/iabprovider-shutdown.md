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
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348899"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="d4595-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="d4595-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="d4595-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4595-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4595-105">Cancela uma conexão com uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="d4595-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d4595-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4595-106">Parameters</span></span>

 <span data-ttu-id="d4595-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4595-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d4595-108">No Serve deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="d4595-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4595-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d4595-109">Return value</span></span>

<span data-ttu-id="d4595-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4595-110">S_OK</span></span> 
  
> <span data-ttu-id="d4595-111">A conexão foi cancelada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d4595-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d4595-112">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="d4595-112">Notes to implementers</span></span>

<span data-ttu-id="d4595-113">Na sua implementação do método **Shutdown** , execute qualquer tarefa que você considere necessário.</span><span class="sxs-lookup"><span data-stu-id="d4595-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="d4595-114">O MAPI chama seu método **Shutdown** somente depois que você lançou todos os objetos de logon.</span><span class="sxs-lookup"><span data-stu-id="d4595-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4595-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4595-115">See also</span></span>



[<span data-ttu-id="d4595-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4595-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

