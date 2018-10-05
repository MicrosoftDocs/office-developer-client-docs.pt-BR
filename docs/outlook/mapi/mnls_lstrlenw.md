---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392085"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="a6ddf-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="a6ddf-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="a6ddf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6ddf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6ddf-105">Determina o comprimento da cadeia Unicode especificado, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="a6ddf-106">Considere o uso [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a6ddf-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="a6ddf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6ddf-107">Parameters</span></span>

 <span data-ttu-id="a6ddf-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a6ddf-108">_lpsz_</span></span>
  
> <span data-ttu-id="a6ddf-109">[in] A sequência de Unicode terminada em nulo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6ddf-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6ddf-110">Return value</span></span>

<span data-ttu-id="a6ddf-111">A função retorna um inteiro com o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="a6ddf-112">É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="a6ddf-113">Se _lpsz_ for NULL, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6ddf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6ddf-114">Remarks</span></span>

<span data-ttu-id="a6ddf-115">Essa função é disposto a função **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="a6ddf-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="a6ddf-116">Para obter mais informações, consulte [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6ddf-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6ddf-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6ddf-117">See also</span></span>



[<span data-ttu-id="a6ddf-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="a6ddf-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="a6ddf-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="a6ddf-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

