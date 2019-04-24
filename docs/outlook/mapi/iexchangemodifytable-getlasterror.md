---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350859"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="e49d4-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e49d4-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="e49d4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e49d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e49d4-105">Retorna informações sobre o último erro que ocorreu em um objeto Table.</span><span class="sxs-lookup"><span data-stu-id="e49d4-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="e49d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e49d4-106">Parameters</span></span>

 <span data-ttu-id="e49d4-107">_And_</span><span class="sxs-lookup"><span data-stu-id="e49d4-107">_hResult_</span></span>
  
> <span data-ttu-id="e49d4-108">no O valor de retorno do método que falhou.</span><span class="sxs-lookup"><span data-stu-id="e49d4-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="e49d4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e49d4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e49d4-110">no Não usado, definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e49d4-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="e49d4-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="e49d4-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e49d4-112">bota Aponta para uma estrutura [MAPIERROR](mapierror.md) MAPI que contém informações sobre o último erro que ocorreu para um objeto Table.</span><span class="sxs-lookup"><span data-stu-id="e49d4-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e49d4-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="e49d4-113">See also</span></span>



[<span data-ttu-id="e49d4-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e49d4-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="e49d4-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e49d4-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="e49d4-116">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e49d4-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

