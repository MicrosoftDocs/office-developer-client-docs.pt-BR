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
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328039"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="a7be9-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="a7be9-103">FPropContainsProp</span></span>

<span data-ttu-id="a7be9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7be9-105">Compara dois valores de propriedade, geralmente cadeias de caracteres ou matrizes binárias, para ver se um contém o outro.</span><span class="sxs-lookup"><span data-stu-id="a7be9-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7be9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a7be9-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7be9-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a7be9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a7be9-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a7be9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a7be9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7be9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a7be9-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a7be9-110">Called by:</span></span>  <br/> |<span data-ttu-id="a7be9-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a7be9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="a7be9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7be9-112">Parameters</span></span>

<span data-ttu-id="a7be9-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="a7be9-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="a7be9-114">no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define o valor da propriedade que pode conter a cadeia de caracteres de pesquisa apontada pelo parâmetro _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="a7be9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="a7be9-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="a7be9-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="a7be9-116">no Ponteiro para uma estrutura **SPropValue** que define a cadeia de caracteres de pesquisa que **FPropContainsProp** está procurando no valor da propriedade apontado pelo parâmetro _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="a7be9-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="a7be9-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="a7be9-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="a7be9-118">no Configurações de opção que definem o nível de precisão a ser usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="a7be9-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="a7be9-119">Os **16 bits inferiores** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="a7be9-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="a7be9-120">Eles devem ser configurados exatamente como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a7be9-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="a7be9-121">FL_FULLSTRING: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve ser igual ao valor da propriedade identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="a7be9-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="a7be9-122">FL_PREFIX: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve aparecer no início do valor da propriedade identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="a7be9-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="a7be9-123">Os dois valores devem ser comparados apenas até o comprimento da cadeia de caracteres de pesquisa indicada por _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="a7be9-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="a7be9-124">FL_SUBSTRING: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve estar contida em qualquer lugar no valor da propriedade identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="a7be9-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="a7be9-125">Os **16 bits superiores** se aplicam apenas às propriedades do tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="a7be9-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="a7be9-126">Eles podem ser definidos com os seguintes valores em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="a7be9-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="a7be9-127">FL_IGNORECASE: a comparação deve ser feita sem considerar a confidencialidade de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7be9-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="a7be9-128">FL_IGNORENONSPACE: a comparação deve ignorar caracteres não espaçados Unicode definidos como marcas diacríticos.</span><span class="sxs-lookup"><span data-stu-id="a7be9-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="a7be9-129">FL_LOOSE: a comparação deve indicar uma coincidência sempre que possível, ignorando os caracteres de diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7be9-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7be9-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a7be9-130">Return value</span></span>

<span data-ttu-id="a7be9-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="a7be9-131">TRUE</span></span> 
  
> <span data-ttu-id="a7be9-132">Os parâmetros são todos válidos e a cadeia de caracteres de pesquisa do _lpSPropValueSrc_ está contida como especificado no valor da propriedade _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="a7be9-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="a7be9-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="a7be9-133">FALSE</span></span> 
  
> <span data-ttu-id="a7be9-134">Os valores de propriedade comparados não são do tipo PT_STRING8 ou PT_BINARY, os valores de propriedade são de tipos diferentes ou a sequência de caracteres de pesquisa do _lpSPropValueSrc_ não está contida como especificado no valor da propriedade _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="a7be9-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a7be9-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7be9-135">Remarks</span></span>

<span data-ttu-id="a7be9-136">O método Comparison depende dos tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) e o heurístico de nível difuso fornecido no parâmetro _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="a7be9-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="a7be9-137">As funções [FPropCompareProp](fpropcompareprop.md) e **FPropContainsProp** podem ser usadas para preparar restrições para a geração de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="a7be9-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="a7be9-138">Os 16 bits superiores de _ulFuzzyLevel_ são ignorados para o tipo de propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="a7be9-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="a7be9-139">Se as configurações no _ulFuzzyLevel_ estiverem ausentes ou forem inválidas, uma correspondência exata de cadeia de caracteres completa será executada.</span><span class="sxs-lookup"><span data-stu-id="a7be9-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="a7be9-140">Para obter mais informações sobre a contenção de propriedade, consulte a estrutura [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="a7be9-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

