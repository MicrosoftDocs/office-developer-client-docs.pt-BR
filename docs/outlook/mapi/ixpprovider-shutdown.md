---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592602"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="ba9d7-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="ba9d7-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="ba9d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba9d7-105">Fecha para baixo de um provedor de transporte de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="ba9d7-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ba9d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba9d7-106">Parameters</span></span>

 <span data-ttu-id="ba9d7-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="ba9d7-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="ba9d7-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ba9d7-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba9d7-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ba9d7-109">Return value</span></span>

<span data-ttu-id="ba9d7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba9d7-110">S_OK</span></span> 
  
> <span data-ttu-id="ba9d7-111">A chamada teve êxito em desligar o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ba9d7-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba9d7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba9d7-112">Remarks</span></span>

<span data-ttu-id="ba9d7-113">O MAPI spooler chama o método **IXPProvider::Shutdown** antes de liberar um objeto de provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ba9d7-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="ba9d7-114">Antes de chamar o **desligamento**, MAPI libera todos os objetos de logon para um provedor.</span><span class="sxs-lookup"><span data-stu-id="ba9d7-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba9d7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba9d7-115">See also</span></span>



[<span data-ttu-id="ba9d7-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="ba9d7-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="ba9d7-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba9d7-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

