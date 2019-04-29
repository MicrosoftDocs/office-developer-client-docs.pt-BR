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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409780"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="3b082-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="3b082-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="3b082-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b082-105">Cancela uma conexão com uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="3b082-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3b082-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b082-106">Parameters</span></span>

 <span data-ttu-id="3b082-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b082-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="3b082-108">No Serve deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="3b082-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b082-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b082-109">Return value</span></span>

<span data-ttu-id="3b082-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b082-110">S_OK</span></span> 
  
> <span data-ttu-id="3b082-111">A conexão foi cancelada com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b082-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="3b082-112">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="3b082-112">Notes to implementers</span></span>

<span data-ttu-id="3b082-113">Na sua implementação do método **Shutdown** , execute qualquer tarefa que você considere necessário.</span><span class="sxs-lookup"><span data-stu-id="3b082-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="3b082-114">O MAPI chama seu método **Shutdown** somente depois que você lançou todos os objetos de logon.</span><span class="sxs-lookup"><span data-stu-id="3b082-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b082-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b082-115">See also</span></span>



[<span data-ttu-id="3b082-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b082-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

