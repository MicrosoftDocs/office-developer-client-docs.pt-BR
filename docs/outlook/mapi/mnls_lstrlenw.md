---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Última modificação: 21 de fevereiro de 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338462"
---
# <a name="mnls_lstrlenw"></a><span data-ttu-id="7825d-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="7825d-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="7825d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7825d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7825d-105">Determina o comprimento da cadeia de caracteres Unicode especificada, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="7825d-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="7825d-106">Considere usar [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7825d-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="7825d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7825d-107">Parameters</span></span>

 <span data-ttu-id="7825d-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="7825d-108">_lpsz_</span></span>
  
> <span data-ttu-id="7825d-109">[in] A cadeia de caracteres Unicode terminada por caractere nulo a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="7825d-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7825d-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7825d-110">Return value</span></span>

<span data-ttu-id="7825d-111">A função retorna um inteiro com o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7825d-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="7825d-112">É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="7825d-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="7825d-113">Se  _lpsz_ for NULL, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7825d-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7825d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7825d-114">Remarks</span></span>

<span data-ttu-id="7825d-115">Esta função quebra a **função lstrlen.**</span><span class="sxs-lookup"><span data-stu-id="7825d-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="7825d-116">Para obter mais informações, consulte [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7825d-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7825d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7825d-117">See also</span></span>



[<span data-ttu-id="7825d-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="7825d-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="7825d-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="7825d-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

