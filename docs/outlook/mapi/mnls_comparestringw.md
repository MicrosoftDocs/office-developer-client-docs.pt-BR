---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Modificado pela última vez: 20 de fevereiro de 2012'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576173"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="dc1fa-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="dc1fa-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="dc1fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc1fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc1fa-105">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="dc1fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc1fa-106">Parameters</span></span>

 <span data-ttu-id="dc1fa-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-107">_lcid_</span></span>
  
> <span data-ttu-id="dc1fa-108">[in] Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-108">[in] Locale identifier.</span></span> <span data-ttu-id="dc1fa-109">Para obter definições detalhadas, consulte o parâmetro _Locale_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc1fa-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="dc1fa-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-110">_dwFlags_</span></span>
  
> <span data-ttu-id="dc1fa-111">[in] Sinalizadores para Ignorar maiusculas/minúsculas e sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="dc1fa-112">Para obter definições detalhadas, consulte o parâmetro _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc1fa-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="dc1fa-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-113">_pstr1_</span></span>
  
> <span data-ttu-id="dc1fa-114">[in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="dc1fa-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-115">_cch1_</span></span>
  
> <span data-ttu-id="dc1fa-116">[in] Comprimento em caracteres da primeira cadeia de caracteres Unicode, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="dc1fa-117">O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="dc1fa-118">Nesse caso, a função **MNLS_CompareStringW** determina o comprimento automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="dc1fa-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-119">_pstr2_</span></span>
  
> <span data-ttu-id="dc1fa-120">[in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="dc1fa-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="dc1fa-121">_cch2_</span></span>
  
> <span data-ttu-id="dc1fa-122">[in] Comprimento em caracteres da segunda cadeia de caracteres Unicode, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="dc1fa-123">O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="dc1fa-124">Nesse caso, a função determina o comprimento automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dc1fa-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc1fa-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dc1fa-125">Return value</span></span>

<span data-ttu-id="dc1fa-126">Retorna os valores descritos para [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc1fa-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc1fa-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc1fa-127">Remarks</span></span>

<span data-ttu-id="dc1fa-128">Essa função distribui [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc1fa-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="dc1fa-129">**MNLS_CompareStringW** usa os mesmos parâmetros e tem o mesmo comportamento como [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc1fa-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc1fa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc1fa-130">See also</span></span>



[<span data-ttu-id="dc1fa-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="dc1fa-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="dc1fa-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="dc1fa-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

