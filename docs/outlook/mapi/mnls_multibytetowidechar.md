---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768145"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="b9cf2-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="b9cf2-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="b9cf2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9cf2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9cf2-105">Semelhante ao **MultiByteToWideChar**, que mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caracteres longa).</span><span class="sxs-lookup"><span data-stu-id="b9cf2-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="b9cf2-106">A cadeia de caracteres não é necessariamente a partir de um caractere multibyte definida.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="b9cf2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9cf2-107">Parameters</span></span>

 <span data-ttu-id="b9cf2-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-108">_uCodePage_</span></span>
  
> <span data-ttu-id="b9cf2-109">[in] Página de código a ser usada na execução da conversão.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="b9cf2-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-110">_dwFlags_</span></span>
  
> <span data-ttu-id="b9cf2-111">[in] Sinalizadores que indica o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="b9cf2-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="b9cf2-113">[in] Ponteiro para a cadeia de caracteres para converter.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="b9cf2-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="b9cf2-115">[in] Tamanho, em bytes, da cadeia de caracteres indicado pelo parâmetro _lpMultiByteStr_ .</span><span class="sxs-lookup"><span data-stu-id="b9cf2-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="b9cf2-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="b9cf2-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-117">[out] Optional.</span></span> <span data-ttu-id="b9cf2-118">Ponteiro para um buffer que recebe a sequência convertida.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="b9cf2-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="b9cf2-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="b9cf2-120">[in] Tamanho, em caracteres, do buffer indicado pelo _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9cf2-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b9cf2-121">Return value</span></span>

<span data-ttu-id="b9cf2-122">Retorna o número de caracteres gravada no buffer indicado pelo _lpWideCharStr_ se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="b9cf2-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9cf2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9cf2-123">Remarks</span></span>

<span data-ttu-id="b9cf2-124">Essa função é disposto a função **MultiByteToWideChar** .</span><span class="sxs-lookup"><span data-stu-id="b9cf2-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="b9cf2-125">Para obter mais informações, consulte [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9cf2-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  
