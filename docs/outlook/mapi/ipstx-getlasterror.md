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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315096"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="bbc9d-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="bbc9d-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="bbc9d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbc9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbc9d-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="bbc9d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbc9d-106">Parameters</span></span>

 <span data-ttu-id="bbc9d-107">_And_</span><span class="sxs-lookup"><span data-stu-id="bbc9d-107">_hResult_</span></span>
  
>  <span data-ttu-id="bbc9d-108">no Código de erro.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="bbc9d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbc9d-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="bbc9d-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="bbc9d-111">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-111">This must be 0.</span></span> 
    
 <span data-ttu-id="bbc9d-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="bbc9d-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="bbc9d-113">bota Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas do erro.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="bbc9d-114">Consulte mapidefs. h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="bbc9d-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bbc9d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbc9d-115">See also</span></span>



[<span data-ttu-id="bbc9d-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="bbc9d-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="bbc9d-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="bbc9d-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

