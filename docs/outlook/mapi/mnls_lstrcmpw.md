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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386345"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="04dea-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="04dea-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="04dea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04dea-105">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="04dea-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="04dea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04dea-106">Parameters</span></span>

 <span data-ttu-id="04dea-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="04dea-107">_lpString1_</span></span>
  
> <span data-ttu-id="04dea-108">[in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="04dea-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="04dea-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="04dea-109">_lpString2_</span></span>
  
> <span data-ttu-id="04dea-110">[in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="04dea-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04dea-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="04dea-111">Return value</span></span>

<span data-ttu-id="04dea-112">Retorna os valores descritos para uma chamada para **MNLS_CompareStringW** , exceto CSTR_EQUAL um equivalente.</span><span class="sxs-lookup"><span data-stu-id="04dea-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04dea-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="04dea-113">Remarks</span></span>

 <span data-ttu-id="04dea-114">_MNLS_lstrcmpW_ executa uma comparação chamando [MNLS_CompareStringW](mnls_comparestringw.md) com uma localidade em GetUserDefaultLCID, 0 para sinalizadores e -1 para cch1 e cch2.</span><span class="sxs-lookup"><span data-stu-id="04dea-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04dea-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="04dea-115">See also</span></span>



[<span data-ttu-id="04dea-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="04dea-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

