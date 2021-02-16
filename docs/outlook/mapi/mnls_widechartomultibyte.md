---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338728"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="e8796-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="e8796-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="e8796-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8796-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8796-105">Esta função é semelhante a **WideCharToMultiByte**, que mapeia uma cadeia de caracteres UTF-16 (caractere largo) para uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8796-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="e8796-106">A nova cadeia de caracteres não é necessariamente de um conjunto de caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="e8796-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="e8796-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8796-107">Parameters</span></span>

 <span data-ttu-id="e8796-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="e8796-108">_uCodePage_</span></span>
  
> <span data-ttu-id="e8796-109">[in] Página de código a ser usada na execução da conversão.</span><span class="sxs-lookup"><span data-stu-id="e8796-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="e8796-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e8796-110">_dwFlags_</span></span>
  
> <span data-ttu-id="e8796-111">[in] Sinalizadores indicando o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="e8796-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="e8796-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="e8796-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="e8796-113">[in] Ponteiro para a cadeia de caracteres Unicode a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="e8796-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="e8796-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="e8796-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="e8796-115">[in] Sinalizadores indicando o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="e8796-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="e8796-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="e8796-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="e8796-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="e8796-117">[out] Optional.</span></span> <span data-ttu-id="e8796-118">Ponteiro para um buffer que recebe a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="e8796-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="e8796-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="e8796-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="e8796-120">[in] Tamanho, em bytes, do buffer indicado por  _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="e8796-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="e8796-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="e8796-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="e8796-122">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="e8796-122">[in] Optional.</span></span> <span data-ttu-id="e8796-123">Ponteiro para o caractere a ser usado se um caractere não puder ser representado na página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="e8796-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="e8796-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="e8796-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="e8796-125">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="e8796-125">[out] Optional.</span></span> <span data-ttu-id="e8796-126">Ponteiro para um sinalizador que indica se a função usou um caractere padrão na conversão.</span><span class="sxs-lookup"><span data-stu-id="e8796-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8796-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e8796-127">Return value</span></span>

<span data-ttu-id="e8796-128">Retorna o número de bytes gravados no buffer apontado por  _lpMultiByteStr,_ se bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e8796-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8796-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8796-129">Remarks</span></span>

<span data-ttu-id="e8796-130">Esta função envolve a **função WideCharToMultiByte.**</span><span class="sxs-lookup"><span data-stu-id="e8796-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="e8796-131">Para obter mais informações, [consulte WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8796-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8796-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8796-132">See also</span></span>



[<span data-ttu-id="e8796-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="e8796-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

