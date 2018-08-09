---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Modificado pela última vez: 18 de junho de 2012'
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768136"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="55af6-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="55af6-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="55af6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55af6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55af6-105">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="55af6-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="55af6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55af6-106">Parameters</span></span>

 <span data-ttu-id="55af6-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="55af6-107">_lpString1_</span></span>
  
> <span data-ttu-id="55af6-108">[in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="55af6-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="55af6-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="55af6-109">_lpString2_</span></span>
  
> <span data-ttu-id="55af6-110">[in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="55af6-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55af6-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="55af6-111">Return value</span></span>

<span data-ttu-id="55af6-112">Retorna os valores descritos para uma chamada para **MNLS_CompareStringW** , exceto CSTR_EQUAL um equivalente.</span><span class="sxs-lookup"><span data-stu-id="55af6-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55af6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55af6-113">Remarks</span></span>

 <span data-ttu-id="55af6-114">_MNLS_lstrcmpW_ executa uma comparação chamando [MNLS_CompareStringW](mnls_comparestringw.md) com uma localidade em GetUserDefaultLCID, 0 para sinalizadores e -1 para cch1 e cch2.</span><span class="sxs-lookup"><span data-stu-id="55af6-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55af6-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="55af6-115">See also</span></span>



[<span data-ttu-id="55af6-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="55af6-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

