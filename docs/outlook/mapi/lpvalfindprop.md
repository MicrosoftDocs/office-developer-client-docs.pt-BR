---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578091"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="d5d4e-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="d5d4e-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="d5d4e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5d4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5d4e-105">Procura uma propriedade especificada em uma propriedade definida.</span><span class="sxs-lookup"><span data-stu-id="d5d4e-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5d4e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d5d4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5d4e-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d5d4e-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d5d4e-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d5d4e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5d4e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d5d4e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d5d4e-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d5d4e-110">Called by:</span></span>  <br/> |<span data-ttu-id="d5d4e-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="d5d4e-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="d5d4e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5d4e-112">Parameters</span></span>

 <span data-ttu-id="d5d4e-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d5d4e-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="d5d4e-114">[in] Marca para a propriedade pesquisar no conjunto de propriedades, indicado pelo parâmetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="d5d4e-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d5d4e-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="d5d4e-115">_cValues_</span></span>
  
> <span data-ttu-id="d5d4e-116">[in] Contagem de propriedades no conjunto de propriedades, indicado pelo parâmetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="d5d4e-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d5d4e-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="d5d4e-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="d5d4e-118">[in] Matriz de estruturas de **SPropValue** que define as propriedades a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="d5d4e-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5d4e-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d5d4e-119">Return value</span></span>

<span data-ttu-id="d5d4e-120">A função **LpValFindProp** retorna uma estrutura **SPropValue** que define a propriedade que corresponda a propriedade input marca ou NULL se não houver nenhuma correspondência.</span><span class="sxs-lookup"><span data-stu-id="d5d4e-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d5d4e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5d4e-121">Remarks</span></span>

<span data-ttu-id="d5d4e-122">A função **LpValFindProp** é idêntica ao **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="d5d4e-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5d4e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5d4e-123">See also</span></span>



[<span data-ttu-id="d5d4e-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="d5d4e-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="d5d4e-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d5d4e-125">SPropValue</span></span>](spropvalue.md)

