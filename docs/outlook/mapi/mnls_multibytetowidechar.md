---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338238"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="cc6bf-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="cc6bf-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="cc6bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc6bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc6bf-105">Semelhante a **MultiByteToWideChar**, que mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caractere largo).</span><span class="sxs-lookup"><span data-stu-id="cc6bf-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="cc6bf-106">A cadeia de caracteres não é necessariamente de um conjunto de caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="cc6bf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc6bf-107">Parameters</span></span>

 <span data-ttu-id="cc6bf-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-108">_uCodePage_</span></span>
  
> <span data-ttu-id="cc6bf-109">[in] Página de código a ser usada na execução da conversão.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="cc6bf-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-110">_dwFlags_</span></span>
  
> <span data-ttu-id="cc6bf-111">[in] Sinalizadores que indicam o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="cc6bf-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="cc6bf-113">[in] Ponteiro para a cadeia de caracteres a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="cc6bf-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="cc6bf-115">[in] Tamanho, em bytes, da cadeia de caracteres indicada pelo parâmetro _lpMultiByteStr._</span><span class="sxs-lookup"><span data-stu-id="cc6bf-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="cc6bf-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="cc6bf-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-117">[out] Optional.</span></span> <span data-ttu-id="cc6bf-118">Ponteiro para um buffer que recebe a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="cc6bf-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="cc6bf-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="cc6bf-120">[in] Tamanho, em caracteres, do buffer indicado por  _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc6bf-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cc6bf-121">Return value</span></span>

<span data-ttu-id="cc6bf-122">Retorna o número de caracteres gravados no buffer indicado por  _lpWideCharStr,_ se bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc6bf-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc6bf-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc6bf-123">Remarks</span></span>

<span data-ttu-id="cc6bf-124">Esta função envolve a **função MultiByteToWideChar.**</span><span class="sxs-lookup"><span data-stu-id="cc6bf-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="cc6bf-125">Para obter mais informações, [consulte MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc6bf-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

