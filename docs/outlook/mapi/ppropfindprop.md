---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565652"
---
# <a name="ppropfindprop"></a><span data-ttu-id="0caf5-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="0caf5-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="0caf5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0caf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0caf5-105">Procura uma propriedade especificada em uma propriedade definida.</span><span class="sxs-lookup"><span data-stu-id="0caf5-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0caf5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0caf5-106">Header file:</span></span>  <br/> |<span data-ttu-id="0caf5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0caf5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0caf5-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0caf5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0caf5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0caf5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0caf5-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0caf5-110">Called by:</span></span>  <br/> |<span data-ttu-id="0caf5-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0caf5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="0caf5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0caf5-112">Parameters</span></span>

 <span data-ttu-id="0caf5-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="0caf5-113">_rgprop_</span></span>
  
> <span data-ttu-id="0caf5-114">[in] Matriz de estruturas de [SPropValue](spropvalue.md) que definem as propriedades a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="0caf5-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="0caf5-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="0caf5-115">_cprop_</span></span>
  
> <span data-ttu-id="0caf5-116">[in] Contagem de propriedades no conjunto de propriedade indicada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="0caf5-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0caf5-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0caf5-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="0caf5-118">[in] Marca de propriedade para a propriedade pesquisar no conjunto de propriedades indicado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="0caf5-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0caf5-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0caf5-119">Return value</span></span>

 <span data-ttu-id="0caf5-120">**PpropFindProp** retorna uma estrutura de [SPropValue](spropvalue.md) definindo a propriedade que corresponda a propriedade input marca ou NULL se não houver nenhuma correspondência.</span><span class="sxs-lookup"><span data-stu-id="0caf5-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0caf5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0caf5-121">Remarks</span></span>

<span data-ttu-id="0caf5-122">Se a marca de propriedade determinado indica uma propriedade do tipo PT_UNSPECIFIED, a função **PpropFindProp** localiza uma correspondência apenas para o identificador de propriedade da marca.</span><span class="sxs-lookup"><span data-stu-id="0caf5-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="0caf5-123">Caso contrário, ele encontra uma correspondência para a marca de propriedade inteira, incluindo o tipo de propriedade e retorna a propriedade identificada.</span><span class="sxs-lookup"><span data-stu-id="0caf5-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0caf5-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0caf5-124">MFCMAPI reference</span></span>

<span data-ttu-id="0caf5-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0caf5-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0caf5-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0caf5-126">**File**</span></span>|<span data-ttu-id="0caf5-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="0caf5-127">**Function**</span></span>|<span data-ttu-id="0caf5-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0caf5-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0caf5-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="0caf5-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0caf5-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="0caf5-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="0caf5-131">MFCMAPI usa o método **PpropFindProp** para localizar propriedades em uma propriedade definidas que está sendo adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="0caf5-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0caf5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0caf5-132">See also</span></span>



[<span data-ttu-id="0caf5-133">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0caf5-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

