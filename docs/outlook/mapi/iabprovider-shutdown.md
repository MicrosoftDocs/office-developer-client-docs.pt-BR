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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766859"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="fd472-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="fd472-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="fd472-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd472-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd472-105">Cancela uma conexão para uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="fd472-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fd472-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd472-106">Parameters</span></span>

 <span data-ttu-id="fd472-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd472-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="fd472-108">[In] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="fd472-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd472-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fd472-109">Return value</span></span>

<span data-ttu-id="fd472-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd472-110">S_OK</span></span> 
  
> <span data-ttu-id="fd472-111">A conexão foi cancelada com êxito.</span><span class="sxs-lookup"><span data-stu-id="fd472-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="fd472-112">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="fd472-112">Notes to implementers</span></span>

<span data-ttu-id="fd472-113">Em sua implementação do método **desligamento** , execute as tarefas que você considerar necessário.</span><span class="sxs-lookup"><span data-stu-id="fd472-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="fd472-114">MAPI chama seu método de **desligamento** somente depois de você ter lançado todos os seus objetos de logon.</span><span class="sxs-lookup"><span data-stu-id="fd472-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd472-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd472-115">See also</span></span>



[<span data-ttu-id="fd472-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd472-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

