---
title: Seção do arquivo de configuração de formulários [Propriedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421288"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="78c91-103">Seção do arquivo de configuração de formulários [Propriedades]</span><span class="sxs-lookup"><span data-stu-id="78c91-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="78c91-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78c91-105">A seção **[Propriedades]** lista o conjunto completo de propriedades que o formulário usa e publica; ou seja, as propriedades que ele cria em suas mensagens personalizadas que os aplicativos cliente MAPI podem usar ao exibir colunas, filtrar tabelas de conteúdo, configurar pastas de resultados de pesquisa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="78c91-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="78c91-106">Cada entrada nessa lista de propriedades faz referência a uma subseqüente **[Property.**</span><span class="sxs-lookup"><span data-stu-id="78c91-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="78c91-107">_cadeia de caracteres_ **]** como mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="78c91-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="78c91-108">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="78c91-108">**[Properties]**</span></span>
  
 <span data-ttu-id="78c91-109">**Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="78c91-109">**Property.**</span></span> <span data-ttu-id="78c91-110">__ cadeia de caracteres String__  =  </span><span class="sxs-lookup"><span data-stu-id="78c91-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="78c91-111">O formato de uma **Propriedade [.**</span><span class="sxs-lookup"><span data-stu-id="78c91-111">The format of a [ **Property.**</span></span> <span data-ttu-id="78c91-112">_cadeia de caracteres_] seção é:</span><span class="sxs-lookup"><span data-stu-id="78c91-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="78c91-113">**Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="78c91-113">**[Property.**</span></span> <span data-ttu-id="78c91-114">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="78c91-114">_string_ **]**</span></span>
  
 <span data-ttu-id="78c91-115">**Tipo** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="78c91-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="78c91-116">\*\*\*\* =  _GUID_ NmidPropset</span><span class="sxs-lookup"><span data-stu-id="78c91-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="78c91-117">\*\*\*\* =  _Cadeia de caracteres_ NmidString</span><span class="sxs-lookup"><span data-stu-id="78c91-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="78c91-118">**NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="78c91-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="78c91-119">\*\*\*\* =  _Cadeia de caracteres_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="78c91-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="78c91-120">\*\*\*\* =  _Inteiro_ de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="78c91-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="78c91-121">**Specialtype** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="78c91-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="78c91-122">\*\*\*\* =  _Cadeia de caracteres_ Enum1</span><span class="sxs-lookup"><span data-stu-id="78c91-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="78c91-123">Cada **[propriedade.**</span><span class="sxs-lookup"><span data-stu-id="78c91-123">Each **[Property.**</span></span> <span data-ttu-id="78c91-124">_cadeia de caracteres_ **]** descreve uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="78c91-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="78c91-125">A entrada **Type** especifica o tipo de propriedade MAPI, por exemplo 3 (PT_I4), da propriedade.</span><span class="sxs-lookup"><span data-stu-id="78c91-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="78c91-126">A entrada **NmidPropset** é opcional; juntamente com a entrada **NmidString** ou a entrada **NmidInteger** , a entrada **NmidPropset** fornece o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="78c91-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="78c91-127">**NmidString** fornece o nome da propriedade, enquanto **NmidInteger** fornece o identificador da propriedade.</span><span class="sxs-lookup"><span data-stu-id="78c91-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="78c91-128">**NmidString** e **NmidInteger** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="78c91-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="78c91-129">Se definido, **NmidPropset** deve conter o nome do conjunto de propriedades; Se estiver ausente, **NmidPropset** é definido como um padrão baseado na seguinte regra: se **NmidInteger** estiver presente e seu valor for menor que 0x8000, **NmidPropset** será definido como PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="78c91-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="78c91-130">Se o valor de **NmidInteger** for definido como um inteiro maior que 0x8000, ou se estiver ausente, **NmidPropset** é definido como PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="78c91-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="78c91-131">A entrada **DisplayName** contém o rótulo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="78c91-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="78c91-132">A \*\*\*\* entrada specialtype, se presente e diferente de zero indica que essa propriedade é uma propriedade especial.</span><span class="sxs-lookup"><span data-stu-id="78c91-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="78c91-133">No momento, o único tipo de propriedade especial definido \*\*\*\* é specialtype = 1, que indica as propriedades enumeradas da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="78c91-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="78c91-134">Se **specialtype** for definido como 1, a entrada **Enum1** referenciará **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="78c91-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="78c91-135">_cadeia de caracteres_ **]** seção.</span><span class="sxs-lookup"><span data-stu-id="78c91-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="78c91-136">Veja a seguir um exemplo de uma seção **[properties]** e de **[Properties.**</span><span class="sxs-lookup"><span data-stu-id="78c91-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="78c91-137">_cadeia de caracteres_ **]** seção.</span><span class="sxs-lookup"><span data-stu-id="78c91-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="78c91-138">A entrada **Enum1** no exemplo anterior faz referência a um **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="78c91-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="78c91-139">_cadeia de caracteres_ **]** seção descrevendo uma enumeração de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="78c91-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="78c91-140">Tal enumeração associa a primeira propriedade na **Propriedade [.**</span><span class="sxs-lookup"><span data-stu-id="78c91-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="78c91-141">_cadeia de caracteres_ **]** com uma propriedade de número inteiro, chamada de índice.</span><span class="sxs-lookup"><span data-stu-id="78c91-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="78c91-142">Tal enumeração também contém uma lista dos possíveis valores que o par de índice de exibição pode assumir.</span><span class="sxs-lookup"><span data-stu-id="78c91-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="78c91-143">A especificação de um tipo de propriedade para a enumeração é desnecessária porque por definição uma entrada **Enum1** sempre tem o tipo PT_I4.</span><span class="sxs-lookup"><span data-stu-id="78c91-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="78c91-144">O formato para o **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="78c91-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="78c91-145">_cadeia de caracteres_ **]** seção é:</span><span class="sxs-lookup"><span data-stu-id="78c91-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="78c91-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="78c91-146">**[Enum1.**</span></span> <span data-ttu-id="78c91-147">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="78c91-147">_string_ **]**</span></span>
  
 <span data-ttu-id="78c91-148">\*\*\*\* =  _GUID_ NmidPropset</span><span class="sxs-lookup"><span data-stu-id="78c91-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="78c91-149">\*\*\*\* =  _Cadeia de caracteres_ NmidString</span><span class="sxs-lookup"><span data-stu-id="78c91-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="78c91-150">**NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="78c91-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="78c91-151">**EnumCount** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="78c91-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="78c91-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="78c91-152">**Val.**</span></span> <span data-ttu-id="78c91-153">_número inteiro_ \*\*. \*\* =  _Cadeia de caracteres_ de exibição</span><span class="sxs-lookup"><span data-stu-id="78c91-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="78c91-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="78c91-154">**Val.**</span></span> <span data-ttu-id="78c91-155">_número inteiro_ \*\*. \*\* =  _Inteiro_ de índice</span><span class="sxs-lookup"><span data-stu-id="78c91-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="78c91-156">A seguir está um exemplo de definição de propriedade para uma propriedade enumerada chamada de risco de incêndio com valores possíveis de baixo, médio e alto.</span><span class="sxs-lookup"><span data-stu-id="78c91-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="78c91-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="78c91-157">**[Enum1.**</span></span> <span data-ttu-id="78c91-158">_cadeia de caracteres_ **]** as seções podem ser usadas por aplicativos para duas finalidades: acelerar a filtragem de propriedades usando o índice em vez da cadeia de caracteres e classificar por uma ordem diferente da ordem alfanumérica dos valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="78c91-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="78c91-159">Por exemplo, a classificação pode ser feita com base na ordem baixa-média-alta em vez da ordem alta-média-baixa.</span><span class="sxs-lookup"><span data-stu-id="78c91-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

