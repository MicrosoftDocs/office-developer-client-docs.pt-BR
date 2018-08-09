---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768155"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="5482c-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="5482c-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="5482c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5482c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5482c-105">Essa função é semelhante ao **WideCharToMultiByte**, que mapeia uma cadeia de caracteres UTF-16 (caracteres longa) para uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5482c-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="5482c-106">A nova cadeia de caracteres não é necessariamente a partir de um caractere multibyte definida.</span><span class="sxs-lookup"><span data-stu-id="5482c-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5482c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5482c-107">Parameters</span></span>

 <span data-ttu-id="5482c-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="5482c-108">_uCodePage_</span></span>
  
> <span data-ttu-id="5482c-109">[in] Página de código a ser usada na execução da conversão.</span><span class="sxs-lookup"><span data-stu-id="5482c-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="5482c-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5482c-110">_dwFlags_</span></span>
  
> <span data-ttu-id="5482c-111">[in] Sinalizadores que indica o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="5482c-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="5482c-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="5482c-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="5482c-113">[in] Ponteiro para a cadeia de caracteres Unicode para converter.</span><span class="sxs-lookup"><span data-stu-id="5482c-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="5482c-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="5482c-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="5482c-115">[in] Sinalizadores que indica o tipo de conversão.</span><span class="sxs-lookup"><span data-stu-id="5482c-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="5482c-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="5482c-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="5482c-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="5482c-117">[out] Optional.</span></span> <span data-ttu-id="5482c-118">Ponteiro para um buffer que recebe a sequência convertida.</span><span class="sxs-lookup"><span data-stu-id="5482c-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="5482c-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="5482c-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="5482c-120">[in] Tamanho, em bytes, do buffer indicado pelo _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="5482c-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="5482c-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="5482c-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="5482c-122">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="5482c-122">[in] Optional.</span></span> <span data-ttu-id="5482c-123">Ponteiro para o caractere a ser utilizado se um caractere não pode ser representado na página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="5482c-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="5482c-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="5482c-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="5482c-125">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="5482c-125">[out] Optional.</span></span> <span data-ttu-id="5482c-126">Ponteiro para um sinalizador que indica se a função tiver usado um caractere padrão na conversão.</span><span class="sxs-lookup"><span data-stu-id="5482c-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5482c-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5482c-127">Return value</span></span>

<span data-ttu-id="5482c-128">Retorna o número de bytes gravados no buffer apontado pela _lpMultiByteStr_ se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5482c-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5482c-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5482c-129">Remarks</span></span>

<span data-ttu-id="5482c-130">Essa função é disposto a função **WideCharToMultiByte** .</span><span class="sxs-lookup"><span data-stu-id="5482c-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="5482c-131">Para obter mais informações, consulte [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5482c-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5482c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5482c-132">See also</span></span>



[<span data-ttu-id="5482c-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="5482c-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

