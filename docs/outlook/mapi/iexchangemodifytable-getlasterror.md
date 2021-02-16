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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424508"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="d7151-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d7151-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="d7151-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7151-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7151-105">Retorna informações sobre o último erro que ocorreu em um objeto table.</span><span class="sxs-lookup"><span data-stu-id="d7151-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="d7151-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7151-106">Parameters</span></span>

 <span data-ttu-id="d7151-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d7151-107">_hResult_</span></span>
  
> <span data-ttu-id="d7151-108">[in] O valor de retorno do método que falhou.</span><span class="sxs-lookup"><span data-stu-id="d7151-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="d7151-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7151-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d7151-110">[in] Não usado, definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d7151-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="d7151-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d7151-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d7151-112">[out] Aponta para uma estrutura [MAPIERROR MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para um objeto de tabela.</span><span class="sxs-lookup"><span data-stu-id="d7151-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d7151-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7151-113">See also</span></span>



[<span data-ttu-id="d7151-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7151-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="d7151-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d7151-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="d7151-116">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d7151-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

