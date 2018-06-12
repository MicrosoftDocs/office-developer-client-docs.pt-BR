---
title: Seção de [Propriedades] do arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766607"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="fa7ef-103">Seção de [Propriedades] do arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="fa7ef-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="fa7ef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa7ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa7ef-105">A seção **[Propriedades]** lista o conjunto completo de propriedades que o formulário usa e publica; ou seja, as propriedades que ele cria em suas mensagens personalizadas que o cliente MAPI aplicativos podem usado ao exibir colunas, a filtragem de tabelas de conteúdo, como configurar pastas de resultados da pesquisa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="fa7ef-106">Cada entrada na lista propriedade faz referência a um subsequentes **[propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="fa7ef-107">_cadeia de caracteres_ seção de **]** conforme mostrado seguinte.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="fa7ef-108">**[Propriedades]**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-108">**[Properties]**</span></span>
  
 <span data-ttu-id="fa7ef-109">**Propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-109">**Property.**</span></span> <span data-ttu-id="fa7ef-110">_cadeia de caracteres_ =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="fa7ef-111">O formato de um [ **propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-111">The format of a [ **Property.**</span></span> <span data-ttu-id="fa7ef-112">_cadeia de caracteres_] seção é:</span><span class="sxs-lookup"><span data-stu-id="fa7ef-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="fa7ef-113">**[Propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-113">**[Property.**</span></span> <span data-ttu-id="fa7ef-114">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-114">_string_ **]**</span></span>
  
 <span data-ttu-id="fa7ef-115">**Tipo** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="fa7ef-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="fa7ef-117">**NmidString** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="fa7ef-118">**Opção NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="fa7ef-119">**DisplayName** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="fa7ef-120">**Sinalizadores** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="fa7ef-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="fa7ef-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="fa7ef-122">**Enum1** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="fa7ef-123">Cada **[propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-123">Each **[Property.**</span></span> <span data-ttu-id="fa7ef-124">_cadeia de caracteres_ seção de **]** descreve uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="fa7ef-125">A entrada de **tipo** Especifica o tipo de propriedade MAPI, por exemplo 3 (PT_I4), da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="fa7ef-126">A entrada **NmidPropset** é opcional. junto com a entrada **NmidString** ou a entrada de **opção NmidInteger** , a entrada **NmidPropset** fornece o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="fa7ef-127">**NmidString** fornece o nome da propriedade, enquanto a **opção NmidInteger** dá o identificador da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="fa7ef-128">**NmidString** e **opção NmidInteger** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="fa7ef-129">Se definido, o **NmidPropset** deve conter o nome do conjunto de propriedades; Se ausente, **NmidPropset** for definido como um padrão com base em que a regra a seguir: se a **opção NmidInteger** estiver presente e seu valor for menor que 0x8000, **NmidPropset** é definido como PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="fa7ef-130">Se o valor da **opção NmidInteger** estiver definido como um número inteiro maior 0x8000, ou se ele está ausente, **NmidPropset** é definido como PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="fa7ef-131">A entrada de **DisplayName** contém o rótulo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="fa7ef-132">A entrada **SpecialType** , se presente, mas diferente de zero indica que esta propriedade é uma propriedade especial.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="fa7ef-133">No momento, o tipo de propriedade apenas especial definido é **SpecialType** = 1, que indica as propriedades de cadeia de caracteres enumerada.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="fa7ef-134">Se **SpecialType** estiver definida como 1, a entrada **Enum1** referencia o **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="fa7ef-135">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="fa7ef-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="fa7ef-136">A seguir está um exemplo de uma seção **[Propriedades]** e um **[Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="fa7ef-137">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="fa7ef-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="fa7ef-138">A entrada **Enum1** nas referências de exemplo anterior para um subsequentes **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="fa7ef-139">_cadeia de caracteres_ seção de **]** descrevendo uma enumeração de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="fa7ef-140">Uma enumeração tal associa a propriedade primeira no **[propriedade.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="fa7ef-141">_cadeia de caracteres_ seção **]** com uma propriedade de inteiro, chamado o índice.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="fa7ef-142">Tal uma enumeração também contém uma lista dos valores possíveis que pode assumir o par de índice de exibição.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="fa7ef-143">Especificar um tipo de propriedade para a enumeração é desnecessário porque, por definição, uma entrada de **Enum1** sempre tem o tipo de PT_I4.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="fa7ef-144">O formato para o **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="fa7ef-145">_cadeia de caracteres_ seção **]** é:</span><span class="sxs-lookup"><span data-stu-id="fa7ef-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="fa7ef-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-146">**[Enum1.**</span></span> <span data-ttu-id="fa7ef-147">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-147">_string_ **]**</span></span>
  
 <span data-ttu-id="fa7ef-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="fa7ef-149">**NmidString** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="fa7ef-150">**Opção NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="fa7ef-151">**EnumCount** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="fa7ef-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-152">**Val.**</span></span> <span data-ttu-id="fa7ef-153">_inteiro_ **. Exibição** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="fa7ef-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-154">**Val.**</span></span> <span data-ttu-id="fa7ef-155">_inteiro_ **. Índice** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="fa7ef-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="fa7ef-156">A seguir está uma definição de propriedade de exemplo para uma propriedade enumerada chamada incêndio risco com os valores possíveis de baixo, médio e alto.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="fa7ef-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fa7ef-157">**[Enum1.**</span></span> <span data-ttu-id="fa7ef-158">_cadeia de caracteres_ seções **]** podem ser usadas por aplicativos para fins de duas: para acelerar a filtragem das propriedades usando o índice, em vez da cadeia de caracteres e classificar por diferente da ordem a ordem alfanumérica dos valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="fa7ef-159">Por exemplo, classificando poderia ser feita com base na ordem de baixo-médio-alto, em vez de ordem alta-Médio-baixo.</span><span class="sxs-lookup"><span data-stu-id="fa7ef-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

