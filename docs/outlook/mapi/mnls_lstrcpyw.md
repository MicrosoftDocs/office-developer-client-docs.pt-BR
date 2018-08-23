---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Modificado pela última vez: 18 de junho de 2012'
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575459"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="491b8-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="491b8-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="491b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="491b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="491b8-105">Copia uma cadeia de caracteres para um buffer.</span><span class="sxs-lookup"><span data-stu-id="491b8-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="491b8-106">Não a use.</span><span class="sxs-lookup"><span data-stu-id="491b8-106">Do not use.</span></span> <span data-ttu-id="491b8-107">Considere o uso [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="491b8-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="491b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="491b8-108">Parameters</span></span>

<span data-ttu-id="491b8-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="491b8-109">lpString1</span></span>
  
> <span data-ttu-id="491b8-110">[out] Um buffer para receber o conteúdo da cadeia de caracteres apontado pelo parâmetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="491b8-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="491b8-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="491b8-111">lpString2</span></span>
  
> <span data-ttu-id="491b8-112">[in] A sequência terminada em nulo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="491b8-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="491b8-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="491b8-113">Return value</span></span>

<span data-ttu-id="491b8-114">Se a função tiver êxito, o valor de retorno é um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="491b8-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="491b8-115">Se a função falhar, o valor de retorno é nulo e lpString1 pode não ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="491b8-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="491b8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="491b8-116">Remarks</span></span>

<span data-ttu-id="491b8-117">Essa função é disposto a função **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="491b8-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="491b8-118">Para obter mais informações, consulte [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="491b8-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="491b8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="491b8-119">See also</span></span>



[<span data-ttu-id="491b8-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="491b8-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

