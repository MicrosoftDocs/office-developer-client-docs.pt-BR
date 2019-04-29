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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414974"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="49311-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="49311-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="49311-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49311-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49311-105">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="49311-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="49311-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49311-106">Parameters</span></span>

 <span data-ttu-id="49311-107">_And_</span><span class="sxs-lookup"><span data-stu-id="49311-107">_hResult_</span></span>
  
>  <span data-ttu-id="49311-108">no Código de erro.</span><span class="sxs-lookup"><span data-stu-id="49311-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="49311-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49311-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="49311-110">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="49311-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="49311-111">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="49311-111">This must be 0.</span></span> 
    
 <span data-ttu-id="49311-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="49311-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="49311-113">bota Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas do erro.</span><span class="sxs-lookup"><span data-stu-id="49311-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="49311-114">Consulte mapidefs. h para a definição de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="49311-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="49311-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="49311-115">See also</span></span>



[<span data-ttu-id="49311-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="49311-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="49311-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="49311-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

