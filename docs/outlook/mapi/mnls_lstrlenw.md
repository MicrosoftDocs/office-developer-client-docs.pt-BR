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
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588885"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="de3df-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="de3df-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="de3df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de3df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de3df-105">Determina o comprimento da cadeia Unicode especificado, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="de3df-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="de3df-106">Considere o uso [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="de3df-106">Consider using [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="de3df-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3df-107">Parameters</span></span>

 <span data-ttu-id="de3df-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="de3df-108">_lpsz_</span></span>
  
> <span data-ttu-id="de3df-109">[in] A sequência de Unicode terminada em nulo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="de3df-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de3df-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="de3df-110">Return value</span></span>

<span data-ttu-id="de3df-111">A função retorna um inteiro com o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="de3df-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="de3df-112">É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="de3df-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="de3df-113">Se _lpsz_ for NULL, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="de3df-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de3df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="de3df-114">Remarks</span></span>

<span data-ttu-id="de3df-115">Essa função é disposto a função **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="de3df-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="de3df-116">Para obter mais informações, consulte [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="de3df-116">For more information, see [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de3df-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="de3df-117">See also</span></span>



[<span data-ttu-id="de3df-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="de3df-118">lstrlen</span></span>](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="de3df-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="de3df-119">StringCchLength</span></span>](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

