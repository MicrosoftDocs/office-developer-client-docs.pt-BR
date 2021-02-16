---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Última modificação: 20 de fevereiro de 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356851"
---
# <a name="mnls_isbadstringptrw"></a><span data-ttu-id="e883b-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="e883b-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="e883b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e883b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e883b-105">Verifica se um ponteiro para uma cadeia de caracteres larga é válido.</span><span class="sxs-lookup"><span data-stu-id="e883b-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="e883b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e883b-106">Parameters</span></span>

 <span data-ttu-id="e883b-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e883b-107">_lpsz_</span></span>
  
> <span data-ttu-id="e883b-108">[in] Um ponteiro para a cadeia de caracteres larga.</span><span class="sxs-lookup"><span data-stu-id="e883b-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="e883b-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="e883b-109">_ucchMax_</span></span>
  
> <span data-ttu-id="e883b-110">[in] O comprimento máximo da cadeia de caracteres em caracteres, incluindo o terminador.</span><span class="sxs-lookup"><span data-stu-id="e883b-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e883b-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e883b-111">Return value</span></span>

<span data-ttu-id="e883b-112">Retorna um Boolean que será true se a cadeia de caracteres for ruim.</span><span class="sxs-lookup"><span data-stu-id="e883b-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e883b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e883b-113">Remarks</span></span>

<span data-ttu-id="e883b-114">Esta função quebra [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e883b-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="e883b-115">Para obter mais informações, consulte [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e883b-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

