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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419636"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="efe00-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="efe00-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="efe00-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efe00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efe00-105">Pesquisa uma propriedade especificada em um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="efe00-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efe00-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="efe00-106">Header file:</span></span>  <br/> |<span data-ttu-id="efe00-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="efe00-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="efe00-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="efe00-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="efe00-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="efe00-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="efe00-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="efe00-110">Called by:</span></span>  <br/> |<span data-ttu-id="efe00-111">Aplicativos cliente e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="efe00-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="efe00-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efe00-112">Parameters</span></span>

 <span data-ttu-id="efe00-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="efe00-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="efe00-114">[in] Marca para a propriedade a ser pesquisada no conjunto de propriedades, indicado pelo parâmetro _lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="efe00-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="efe00-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="efe00-115">_cValues_</span></span>
  
> <span data-ttu-id="efe00-116">[in] Contagem de propriedades no conjunto de propriedades, indicada pelo parâmetro _lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="efe00-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="efe00-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="efe00-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="efe00-118">[in] Matriz de **estruturas SPropValue** que define as propriedades a serem pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="efe00-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="efe00-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="efe00-119">Return value</span></span>

<span data-ttu-id="efe00-120">A **função LpValFindProp** retorna uma estrutura **SPropValue** que define a propriedade que corresponde à marca de propriedade de entrada ou NULL se não houver nenhuma combinação.</span><span class="sxs-lookup"><span data-stu-id="efe00-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="efe00-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe00-121">Remarks</span></span>

<span data-ttu-id="efe00-122">A **função LpValFindProp** é idêntica a **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="efe00-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efe00-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe00-123">See also</span></span>



[<span data-ttu-id="efe00-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="efe00-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="efe00-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="efe00-125">SPropValue</span></span>](spropvalue.md)

