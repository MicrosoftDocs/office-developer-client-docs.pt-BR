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
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398735"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="35304-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="35304-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="35304-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35304-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35304-105">Verifica se um ponteiro para uma cadeia de caracteres longa é válido.</span><span class="sxs-lookup"><span data-stu-id="35304-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="35304-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35304-106">Parameters</span></span>

 <span data-ttu-id="35304-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="35304-107">_lpsz_</span></span>
  
> <span data-ttu-id="35304-108">[in] Um ponteiro para a cadeia de caracteres longa.</span><span class="sxs-lookup"><span data-stu-id="35304-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="35304-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="35304-109">_ucchMax_</span></span>
  
> <span data-ttu-id="35304-110">[in] O comprimento máximo da cadeia de caracteres em caracteres, incluindo o terminador.</span><span class="sxs-lookup"><span data-stu-id="35304-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35304-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="35304-111">Return value</span></span>

<span data-ttu-id="35304-112">Retorna um Boolean que será true se a cadeia de caracteres é defeituoso.</span><span class="sxs-lookup"><span data-stu-id="35304-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35304-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="35304-113">Remarks</span></span>

<span data-ttu-id="35304-114">Essa função distribui [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="35304-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="35304-115">Para obter mais informações, consulte [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="35304-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

