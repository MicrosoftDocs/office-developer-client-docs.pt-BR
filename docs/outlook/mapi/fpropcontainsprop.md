---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571672"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="34417-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="34417-103">FPropContainsProp</span></span>

<span data-ttu-id="34417-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34417-105">Compara dois valores de propriedade, geralmente as cadeias de caracteres ou matrizes de binários, para ver se um contém o outro.</span><span class="sxs-lookup"><span data-stu-id="34417-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34417-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="34417-106">Header file:</span></span>  <br/> |<span data-ttu-id="34417-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="34417-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="34417-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="34417-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="34417-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="34417-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="34417-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="34417-110">Called by:</span></span>  <br/> |<span data-ttu-id="34417-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="34417-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="34417-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34417-112">Parameters</span></span>

<span data-ttu-id="34417-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="34417-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="34417-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o valor da propriedade que pode conter a cadeia de caracteres de pesquisa apontado pelo parâmetro _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="34417-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="34417-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="34417-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="34417-116">[in] Ponteiro para uma estrutura **SPropValue** definindo a cadeia de caracteres de pesquisa que **FPropContainsProp** está procurando no valor da propriedade apontado pelo parâmetro _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="34417-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="34417-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="34417-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="34417-118">[in] Configurações de opção definindo o nível de precisão para usar na comparação.</span><span class="sxs-lookup"><span data-stu-id="34417-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="34417-119">Os **16 bits inferiores** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="34417-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="34417-120">Eles devem ser definidos como exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="34417-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="34417-121">FL_FULLSTRING: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve ser igual ao valor da propriedade identificado pela _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="34417-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="34417-122">FL_PREFIX: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deverá aparecer no início do valor da propriedade identificado pela _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="34417-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="34417-123">Os dois valores devem ser comparados somente até o comprimento da cadeia de caracteres de pesquisa indicado pelo _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="34417-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="34417-124">FL_SUBSTRING: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve estar contida em qualquer lugar no valor da propriedade identificado pela _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="34417-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="34417-125">Os **bits de 16 superiores** aplicam-se apenas às propriedades do tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="34417-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="34417-126">Elas podem ser definidas para os seguintes valores em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="34417-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="34417-127">FL_IGNORECASE: Comparação deve ser feita sem considerar a diferenciação de maiusculas.</span><span class="sxs-lookup"><span data-stu-id="34417-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="34417-128">FL_IGNORENONSPACE: Comparação deve ignorar caracteres sem espaçamento definidos pelo Unicode, como sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="34417-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="34417-129">FL_LOOSE: Comparação deve indicar uma correspondência sempre que possível, ignorando caso sensibilidade e caracteres sem espaçamento.</span><span class="sxs-lookup"><span data-stu-id="34417-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34417-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="34417-130">Return value</span></span>

<span data-ttu-id="34417-131">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="34417-131">TRUE</span></span> 
  
> <span data-ttu-id="34417-132">Os parâmetros são válidos e a cadeia de caracteres de pesquisa _lpSPropValueSrc_ está contida conforme especificado no valor da propriedade _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="34417-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="34417-133">FALSO</span><span class="sxs-lookup"><span data-stu-id="34417-133">FALSE</span></span> 
  
> <span data-ttu-id="34417-134">Os valores de propriedade estão sendo comparados não são do tipo PT_STRING8 ou PT_BINARY, os valores de propriedade são de tipos diferentes ou a cadeia de caracteres de pesquisa _lpSPropValueSrc_ não está contida conforme especificado no valor da propriedade _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="34417-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34417-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="34417-135">Remarks</span></span>

<span data-ttu-id="34417-136">O método de comparação depende os tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) e o heurístico nível difuso fornecido no parâmetro _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="34417-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="34417-137">As funções [FPropCompareProp](fpropcompareprop.md) e **FPropContainsProp** podem ser usadas para preparar restrições para gerar uma tabela.</span><span class="sxs-lookup"><span data-stu-id="34417-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="34417-138">Os 16 bits superiores _ulFuzzyLevel_ são ignorados para o tipo de propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="34417-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="34417-139">Se as configurações no _ulFuzzyLevel_ ausente ou inválido, uma correspondência exata da cadeia de caracteres inteira é executada.</span><span class="sxs-lookup"><span data-stu-id="34417-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="34417-140">Para obter mais informações sobre contenção de propriedade, consulte a estrutura [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="34417-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

