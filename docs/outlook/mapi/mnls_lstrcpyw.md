---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Última modificação: 18 de junho de 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341724"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="5bd0d-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="5bd0d-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="5bd0d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bd0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bd0d-105">Copia uma cadeia de caracteres em um buffer.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="5bd0d-106">Não usar.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-106">Do not use.</span></span> <span data-ttu-id="5bd0d-107">Considere usar [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="5bd0d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bd0d-108">Parameters</span></span>

<span data-ttu-id="5bd0d-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="5bd0d-109">lpString1</span></span>
  
> <span data-ttu-id="5bd0d-110">bota Um buffer para receber o conteúdo da cadeia de caracteres apontada pelo parâmetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="5bd0d-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="5bd0d-111">lpString2</span></span>
  
> <span data-ttu-id="5bd0d-112">no A cadeia de caracteres terminada em nulo para ser copiada.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bd0d-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5bd0d-113">Return value</span></span>

<span data-ttu-id="5bd0d-114">Se a função for bem-sucedida, o valor de retorno é um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="5bd0d-115">Se a função falhar, o valor de retorno será NULL e lpString1 não poderá ser finalizado por nulo.</span><span class="sxs-lookup"><span data-stu-id="5bd0d-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bd0d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bd0d-116">Remarks</span></span>

<span data-ttu-id="5bd0d-117">Essa função envolve a função **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="5bd0d-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="5bd0d-118">Para obter mais informações, consulte [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5bd0d-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bd0d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bd0d-119">See also</span></span>



[<span data-ttu-id="5bd0d-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="5bd0d-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

