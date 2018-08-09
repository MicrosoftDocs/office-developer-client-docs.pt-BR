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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 69853dbec46b08c4dc402012fb7f1074f30ebf52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767568"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="f884b-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f884b-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="f884b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f884b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f884b-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="f884b-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="f884b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f884b-106">Parameters</span></span>

 <span data-ttu-id="f884b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f884b-107">_hResult_</span></span>
  
>  <span data-ttu-id="f884b-108">[in] Código de erro.</span><span class="sxs-lookup"><span data-stu-id="f884b-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="f884b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f884b-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="f884b-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="f884b-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="f884b-111">Isso deve ser de 0.</span><span class="sxs-lookup"><span data-stu-id="f884b-111">This must be 0.</span></span> 
    
 <span data-ttu-id="f884b-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f884b-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="f884b-113">[out] Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas para o erro.</span><span class="sxs-lookup"><span data-stu-id="f884b-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="f884b-114">Consulte mapidefs.h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="f884b-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f884b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f884b-115">See also</span></span>



[<span data-ttu-id="f884b-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="f884b-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="f884b-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="f884b-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="f884b-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="f884b-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="f884b-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="f884b-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="f884b-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="f884b-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="f884b-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="f884b-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="f884b-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f884b-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="f884b-123">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f884b-123">MAPI Constants</span></span>](mapi-constants.md)

