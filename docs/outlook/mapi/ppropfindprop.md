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
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350727"
---
# <a name="ppropfindprop"></a><span data-ttu-id="dc5d2-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="dc5d2-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="dc5d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc5d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc5d2-105">Procura por uma propriedade especificada em um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc5d2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dc5d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc5d2-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="dc5d2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dc5d2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dc5d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc5d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc5d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc5d2-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="dc5d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc5d2-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="dc5d2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="dc5d2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc5d2-112">Parameters</span></span>

 <span data-ttu-id="dc5d2-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="dc5d2-113">_rgprop_</span></span>
  
> <span data-ttu-id="dc5d2-114">no Matriz de estruturas [SPropValue](spropvalue.md) que definem as propriedades a serem pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="dc5d2-115">_cProp_</span><span class="sxs-lookup"><span data-stu-id="dc5d2-115">_cprop_</span></span>
  
> <span data-ttu-id="dc5d2-116">no Contagem de propriedades no conjunto de propriedades indicado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="dc5d2-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="dc5d2-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="dc5d2-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="dc5d2-118">no Marca de propriedade da propriedade a ser pesquisada no conjunto de propriedades indicado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="dc5d2-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc5d2-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dc5d2-119">Return value</span></span>

 <span data-ttu-id="dc5d2-120">**PpropFindProp** retorna uma estrutura [SPropValue](spropvalue.md) que define a propriedade que corresponde à marca da propriedade input ou NULL se não houver correspondência.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc5d2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc5d2-121">Remarks</span></span>

<span data-ttu-id="dc5d2-122">Se a marca de propriedade fornecida indicar uma propriedade do tipo PT_UNSPECIFIED, a função **PpropFindProp** localizará uma correspondência somente para o identificador de propriedade na marca.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="dc5d2-123">Caso contrário, ele encontrará uma correspondência para a marca de propriedade inteira, incluindo o tipo de propriedade e retornará a propriedade identificada.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc5d2-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dc5d2-124">MFCMAPI reference</span></span>

<span data-ttu-id="dc5d2-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc5d2-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="dc5d2-126">**File**</span></span>|<span data-ttu-id="dc5d2-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="dc5d2-127">**Function**</span></span>|<span data-ttu-id="dc5d2-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="dc5d2-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc5d2-129">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="dc5d2-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="dc5d2-130">CContentsTableListCtrl:: BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="dc5d2-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="dc5d2-131">MFCMAPI usa o método **PpropFindProp** para localizar Propriedades em um conjunto de propriedades que está sendo adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="dc5d2-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc5d2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc5d2-132">See also</span></span>



[<span data-ttu-id="dc5d2-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="dc5d2-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

