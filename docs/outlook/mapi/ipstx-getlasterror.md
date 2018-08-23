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
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592588"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="7a14d-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7a14d-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="7a14d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a14d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a14d-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="7a14d-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="7a14d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a14d-106">Parameters</span></span>

 <span data-ttu-id="7a14d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="7a14d-107">_hResult_</span></span>
  
>  <span data-ttu-id="7a14d-108">[in] Código de erro.</span><span class="sxs-lookup"><span data-stu-id="7a14d-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="7a14d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a14d-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="7a14d-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="7a14d-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="7a14d-111">Isso deve ser de 0.</span><span class="sxs-lookup"><span data-stu-id="7a14d-111">This must be 0.</span></span> 
    
 <span data-ttu-id="7a14d-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7a14d-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="7a14d-113">[out] Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas para o erro.</span><span class="sxs-lookup"><span data-stu-id="7a14d-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="7a14d-114">Consulte mapidefs.h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="7a14d-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7a14d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a14d-115">See also</span></span>



[<span data-ttu-id="7a14d-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="7a14d-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="7a14d-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="7a14d-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

