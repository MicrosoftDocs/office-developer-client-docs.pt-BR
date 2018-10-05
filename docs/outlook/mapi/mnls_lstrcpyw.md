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
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382705"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="9c2e6-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="9c2e6-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="9c2e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c2e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c2e6-105">Copia uma cadeia de caracteres para um buffer.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="9c2e6-106">Não a use.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-106">Do not use.</span></span> <span data-ttu-id="9c2e6-107">Considere o uso [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9c2e6-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="9c2e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c2e6-108">Parameters</span></span>

<span data-ttu-id="9c2e6-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="9c2e6-109">lpString1</span></span>
  
> <span data-ttu-id="9c2e6-110">[out] Um buffer para receber o conteúdo da cadeia de caracteres apontado pelo parâmetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="9c2e6-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="9c2e6-111">lpString2</span></span>
  
> <span data-ttu-id="9c2e6-112">[in] A sequência terminada em nulo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c2e6-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9c2e6-113">Return value</span></span>

<span data-ttu-id="9c2e6-114">Se a função tiver êxito, o valor de retorno é um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="9c2e6-115">Se a função falhar, o valor de retorno é nulo e lpString1 pode não ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="9c2e6-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c2e6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c2e6-116">Remarks</span></span>

<span data-ttu-id="9c2e6-117">Essa função é disposto a função **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="9c2e6-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="9c2e6-118">Para obter mais informações, consulte [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c2e6-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c2e6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c2e6-119">See also</span></span>



[<span data-ttu-id="9c2e6-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="9c2e6-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

