---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767691"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="9609c-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9609c-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="9609c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9609c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9609c-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="9609c-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="9609c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9609c-106">Parameters</span></span>

 <span data-ttu-id="9609c-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9609c-107">_hResult_</span></span>
  
>  <span data-ttu-id="9609c-108">[in] Código de erro.</span><span class="sxs-lookup"><span data-stu-id="9609c-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="9609c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9609c-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="9609c-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="9609c-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="9609c-111">Isso deve ser de 0.</span><span class="sxs-lookup"><span data-stu-id="9609c-111">This must be 0.</span></span> 
    
 <span data-ttu-id="9609c-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9609c-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="9609c-113">[out] Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas para o erro.</span><span class="sxs-lookup"><span data-stu-id="9609c-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="9609c-114">Consulte mapidefs.h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="9609c-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9609c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9609c-115">See also</span></span>



[<span data-ttu-id="9609c-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="9609c-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="9609c-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="9609c-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

