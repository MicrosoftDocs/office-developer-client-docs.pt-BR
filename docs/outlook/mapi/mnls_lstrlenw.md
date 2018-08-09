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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768166"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="a8d7b-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="a8d7b-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="a8d7b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8d7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8d7b-105">Determina o comprimento da cadeia Unicode especificado, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="a8d7b-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="a8d7b-106">Considere o uso [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a8d7b-106">Consider using [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="a8d7b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8d7b-107">Parameters</span></span>

 <span data-ttu-id="a8d7b-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a8d7b-108">_lpsz_</span></span>
  
> <span data-ttu-id="a8d7b-109">[in] A sequência de Unicode terminada em nulo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="a8d7b-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8d7b-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a8d7b-110">Return value</span></span>

<span data-ttu-id="a8d7b-111">A função retorna um inteiro com o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8d7b-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="a8d7b-112">É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="a8d7b-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="a8d7b-113">Se _lpsz_ for NULL, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a8d7b-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8d7b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8d7b-114">Remarks</span></span>

<span data-ttu-id="a8d7b-115">Essa função é disposto a função **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="a8d7b-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="a8d7b-116">Para obter mais informações, consulte [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8d7b-116">For more information, see [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8d7b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8d7b-117">See also</span></span>



[<span data-ttu-id="a8d7b-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="a8d7b-118">lstrlen</span></span>](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="a8d7b-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="a8d7b-119">StringCchLength</span></span>](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

