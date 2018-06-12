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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766929"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="b2bdf-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b2bdf-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="b2bdf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2bdf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2bdf-105">Retorna informações sobre o último erro que ocorreu em um objeto table.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="b2bdf-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b2bdf-106">Parameters</span></span>

 <span data-ttu-id="b2bdf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b2bdf-107">_hResult_</span></span>
  
> <span data-ttu-id="b2bdf-108">[in] O valor de retorno do método que falharam.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="b2bdf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2bdf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b2bdf-110">[in] Não usado, defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b2bdf-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="b2bdf-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b2bdf-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b2bdf-112">[out] Aponta para uma estrutura MAPI [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para um objeto table.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b2bdf-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2bdf-113">See also</span></span>



[<span data-ttu-id="b2bdf-114">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2bdf-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="b2bdf-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b2bdf-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="b2bdf-116">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b2bdf-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

