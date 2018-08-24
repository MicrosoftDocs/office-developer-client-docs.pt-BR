---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Modificado pela última vez: 20 de fevereiro de 2012'
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589564"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="962ea-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="962ea-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="962ea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="962ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="962ea-105">Verifica se um ponteiro para uma cadeia de caracteres longa é válido.</span><span class="sxs-lookup"><span data-stu-id="962ea-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="962ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="962ea-106">Parameters</span></span>

 <span data-ttu-id="962ea-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="962ea-107">_lpsz_</span></span>
  
> <span data-ttu-id="962ea-108">[in] Um ponteiro para a cadeia de caracteres longa.</span><span class="sxs-lookup"><span data-stu-id="962ea-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="962ea-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="962ea-109">_ucchMax_</span></span>
  
> <span data-ttu-id="962ea-110">[in] O comprimento máximo da cadeia de caracteres em caracteres, incluindo o terminador.</span><span class="sxs-lookup"><span data-stu-id="962ea-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="962ea-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="962ea-111">Return value</span></span>

<span data-ttu-id="962ea-112">Retorna um Boolean que será true se a cadeia de caracteres é defeituoso.</span><span class="sxs-lookup"><span data-stu-id="962ea-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="962ea-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="962ea-113">Remarks</span></span>

<span data-ttu-id="962ea-114">Essa função distribui [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="962ea-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="962ea-115">Para obter mais informações, consulte [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="962ea-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

