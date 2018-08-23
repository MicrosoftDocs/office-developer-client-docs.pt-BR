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
ms.openlocfilehash: 39b4474bcc6bd71993fb5dc42bb2bfc1bf9f5f48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573401"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="31d2d-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="31d2d-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="31d2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31d2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31d2d-105">Certifica-se de que o processo de chamada tem acesso de leitura ao intervalo especificado de memória.</span><span class="sxs-lookup"><span data-stu-id="31d2d-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31d2d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31d2d-106">Header file:</span></span>  <br/> |<span data-ttu-id="31d2d-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="31d2d-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="31d2d-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="31d2d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31d2d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31d2d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31d2d-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="31d2d-110">Called by:</span></span>  <br/> |<span data-ttu-id="31d2d-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="31d2d-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="31d2d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31d2d-112">Parameters</span></span>

 <span data-ttu-id="31d2d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="31d2d-113">_lpsz_</span></span>
  
> <span data-ttu-id="31d2d-114">[in] Ponteiro para uma cadeia de caracteres ASCII terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="31d2d-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="31d2d-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="31d2d-115">_cchMax_</span></span>
  
> <span data-ttu-id="31d2d-116">[in] O tamanho máximo da cadeia de caracteres, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="31d2d-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="31d2d-117">A função verifica para acesso de leitura em todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou até o número de caracteres especificada por esse parâmetro, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="31d2d-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="31d2d-118">Se esse parâmetro for zero, o valor de retorno é zero.</span><span class="sxs-lookup"><span data-stu-id="31d2d-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31d2d-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="31d2d-119">Return value</span></span>

<span data-ttu-id="31d2d-120">O valor de retorno é zero quando o processo de chamada tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="31d2d-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="31d2d-121">O valor de retorno é diferente de zero quando o processo de chamada não tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="31d2d-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31d2d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="31d2d-122">Remarks</span></span>

<span data-ttu-id="31d2d-123">A função **IsBadBoundedStringPtr** é equivalente ao uso **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="31d2d-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31d2d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="31d2d-124">See also</span></span>



[<span data-ttu-id="31d2d-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="31d2d-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

