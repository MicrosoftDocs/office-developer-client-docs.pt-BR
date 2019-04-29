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
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409689"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="5ff30-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="5ff30-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="5ff30-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff30-105">Fecha um provedor de transporte de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="5ff30-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5ff30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ff30-106">Parameters</span></span>

 <span data-ttu-id="5ff30-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ff30-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5ff30-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5ff30-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ff30-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5ff30-109">Return value</span></span>

<span data-ttu-id="5ff30-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ff30-110">S_OK</span></span> 
  
> <span data-ttu-id="5ff30-111">A chamada teve êxito ao desligar o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5ff30-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ff30-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ff30-112">Remarks</span></span>

<span data-ttu-id="5ff30-113">O spooler MAPI chama o método **IXPProvider:: Shutdown** antes de liberar um objeto de provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5ff30-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="5ff30-114">Antes de chamar **Shutdown**, MAPI libera todos os objetos de logon de um provedor.</span><span class="sxs-lookup"><span data-stu-id="5ff30-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ff30-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ff30-115">See also</span></span>



[<span data-ttu-id="5ff30-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="5ff30-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="5ff30-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ff30-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

