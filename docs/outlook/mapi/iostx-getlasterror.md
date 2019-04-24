---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332162"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="5cf0f-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5cf0f-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="5cf0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cf0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cf0f-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="5cf0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cf0f-106">Parameters</span></span>

 <span data-ttu-id="5cf0f-107">_And_</span><span class="sxs-lookup"><span data-stu-id="5cf0f-107">_hResult_</span></span>
  
>  <span data-ttu-id="5cf0f-108">no Código de erro.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="5cf0f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5cf0f-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="5cf0f-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="5cf0f-111">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-111">This must be 0.</span></span> 
    
 <span data-ttu-id="5cf0f-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5cf0f-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="5cf0f-113">bota Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas do erro.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="5cf0f-114">Consulte mapidefs. h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="5cf0f-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5cf0f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cf0f-115">See also</span></span>



[<span data-ttu-id="5cf0f-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="5cf0f-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="5cf0f-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="5cf0f-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="5cf0f-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="5cf0f-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="5cf0f-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="5cf0f-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="5cf0f-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="5cf0f-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="5cf0f-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="5cf0f-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="5cf0f-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5cf0f-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="5cf0f-123">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="5cf0f-123">MAPI Constants</span></span>](mapi-constants.md)

