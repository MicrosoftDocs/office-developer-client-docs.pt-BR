---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356844"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="441b0-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="441b0-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="441b0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="441b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="441b0-105">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="441b0-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="441b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="441b0-106">Parameters</span></span>

 <span data-ttu-id="441b0-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="441b0-107">_lcid_</span></span>
  
> <span data-ttu-id="441b0-108">[in] Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="441b0-108">[in] Locale identifier.</span></span> <span data-ttu-id="441b0-109">Para definições detalhadas, consulte o  _parâmetro Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="441b0-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="441b0-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="441b0-110">_dwFlags_</span></span>
  
> <span data-ttu-id="441b0-111">[in] Sinalizadores para ignorar a ocorrência e os diacríticas.</span><span class="sxs-lookup"><span data-stu-id="441b0-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="441b0-112">Para definições detalhadas, consulte o  _parâmetro dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="441b0-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="441b0-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="441b0-113">_pstr1_</span></span>
  
> <span data-ttu-id="441b0-114">[in] Ponteiro para a primeira cadeia de caracteres Unicode a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="441b0-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="441b0-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="441b0-115">_cch1_</span></span>
  
> <span data-ttu-id="441b0-116">[in] Comprimento em caracteres da primeira cadeia de caracteres Unicode, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="441b0-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="441b0-117">O aplicativo poderá fornecer um valor negativo se a cadeia de caracteres for terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="441b0-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="441b0-118">Nesse caso, a **função MNLS_CompareStringW** determina automaticamente o comprimento.</span><span class="sxs-lookup"><span data-stu-id="441b0-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="441b0-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="441b0-119">_pstr2_</span></span>
  
> <span data-ttu-id="441b0-120">[in] Ponteiro para a segunda cadeia de caracteres Unicode a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="441b0-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="441b0-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="441b0-121">_cch2_</span></span>
  
> <span data-ttu-id="441b0-122">[in] Comprimento em caracteres da segunda cadeia de caracteres Unicode, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="441b0-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="441b0-123">O aplicativo poderá fornecer um valor negativo se a cadeia de caracteres for terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="441b0-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="441b0-124">Nesse caso, a função determina o comprimento automaticamente.</span><span class="sxs-lookup"><span data-stu-id="441b0-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="441b0-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="441b0-125">Return value</span></span>

<span data-ttu-id="441b0-126">Retorna os valores descritos [para CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="441b0-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="441b0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="441b0-127">Remarks</span></span>

<span data-ttu-id="441b0-128">Esta função quebra [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="441b0-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="441b0-129">**MNLS_CompareStringW** aceita os mesmos parâmetros e tem o mesmo comportamento que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="441b0-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="441b0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="441b0-130">See also</span></span>



[<span data-ttu-id="441b0-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="441b0-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="441b0-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="441b0-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

