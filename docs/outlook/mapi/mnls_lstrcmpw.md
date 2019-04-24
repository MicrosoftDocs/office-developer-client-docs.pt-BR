---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Última modificação: 18 de junho de 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356837"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="ced39-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="ced39-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="ced39-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced39-105">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ced39-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="ced39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ced39-106">Parameters</span></span>

 <span data-ttu-id="ced39-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="ced39-107">_lpString1_</span></span>
  
> <span data-ttu-id="ced39-108">no Ponteiro para a primeira cadeia de caracteres Unicode a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ced39-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="ced39-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="ced39-109">_lpString2_</span></span>
  
> <span data-ttu-id="ced39-110">no Ponteiro para a segunda cadeia de caracteres Unicode a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ced39-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ced39-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ced39-111">Return value</span></span>

<span data-ttu-id="ced39-112">Retorna os valores descritos para uma chamada equivalente a **MNLS_CompareStringW** , exceto para CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="ced39-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ced39-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ced39-113">Remarks</span></span>

 <span data-ttu-id="ced39-114">_MNLS_lstrcmpW_ realiza uma comparação chamando [MNLS_CompareStringW](mnls_comparestringw.md) com uma localidade de GetUserDefaultLCID, 0 para sinalizadores e-1 para cch1 e CCH2.</span><span class="sxs-lookup"><span data-stu-id="ced39-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ced39-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ced39-115">See also</span></span>



[<span data-ttu-id="ced39-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="ced39-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

