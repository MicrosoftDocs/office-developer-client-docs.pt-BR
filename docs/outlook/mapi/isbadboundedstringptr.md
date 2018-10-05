---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388900"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="6711b-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="6711b-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="6711b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6711b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6711b-105">Certifica-se de que o processo de chamada tem acesso de leitura ao intervalo especificado de memória.</span><span class="sxs-lookup"><span data-stu-id="6711b-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6711b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6711b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6711b-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="6711b-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="6711b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6711b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6711b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6711b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6711b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6711b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6711b-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="6711b-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="6711b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6711b-112">Parameters</span></span>

 <span data-ttu-id="6711b-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="6711b-113">_lpsz_</span></span>
  
> <span data-ttu-id="6711b-114">[in] Ponteiro para uma cadeia de caracteres ASCII terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6711b-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="6711b-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="6711b-115">_cchMax_</span></span>
  
> <span data-ttu-id="6711b-116">[in] O tamanho máximo da cadeia de caracteres, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="6711b-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="6711b-117">A função verifica para acesso de leitura em todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou até o número de caracteres especificada por esse parâmetro, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="6711b-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="6711b-118">Se esse parâmetro for zero, o valor de retorno é zero.</span><span class="sxs-lookup"><span data-stu-id="6711b-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6711b-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6711b-119">Return value</span></span>

<span data-ttu-id="6711b-120">O valor de retorno é zero quando o processo de chamada tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="6711b-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="6711b-121">O valor de retorno é diferente de zero quando o processo de chamada não tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="6711b-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6711b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6711b-122">Remarks</span></span>

<span data-ttu-id="6711b-123">A função **IsBadBoundedStringPtr** é equivalente ao uso **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="6711b-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6711b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6711b-124">See also</span></span>



[<span data-ttu-id="6711b-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="6711b-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

