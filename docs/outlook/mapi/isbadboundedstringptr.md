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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278831"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="12527-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="12527-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="12527-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12527-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12527-105">Verifica se o processo de chamada tem acesso de leitura ao intervalo de memória especificado.</span><span class="sxs-lookup"><span data-stu-id="12527-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12527-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="12527-106">Header file:</span></span>  <br/> |<span data-ttu-id="12527-107">mapiwin. h</span><span class="sxs-lookup"><span data-stu-id="12527-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="12527-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="12527-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="12527-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="12527-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="12527-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="12527-110">Called by:</span></span>  <br/> |<span data-ttu-id="12527-111">Aplicativos cliente e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="12527-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="12527-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12527-112">Parameters</span></span>

 <span data-ttu-id="12527-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="12527-113">_lpsz_</span></span>
  
> <span data-ttu-id="12527-114">no Ponteiro para uma cadeia de caracteres ASCII terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="12527-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="12527-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="12527-115">_cchMax_</span></span>
  
> <span data-ttu-id="12527-116">no O tamanho máximo da cadeia de caracteres, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="12527-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="12527-117">A função verifica o acesso de leitura em todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou até o número de caracteres especificado por esse parâmetro, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="12527-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="12527-118">Se esse parâmetro for zero, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="12527-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12527-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12527-119">Return value</span></span>

<span data-ttu-id="12527-120">O valor de retorno é zero quando o processo de chamada tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado por _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="12527-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="12527-121">O valor de retorno é diferente de zero quando o processo de chamada não tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado por _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="12527-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12527-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="12527-122">Remarks</span></span>

<span data-ttu-id="12527-123">A função **IsBadBoundedStringPtr** é equivalente ao uso de **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="12527-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12527-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="12527-124">See also</span></span>



[<span data-ttu-id="12527-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="12527-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

