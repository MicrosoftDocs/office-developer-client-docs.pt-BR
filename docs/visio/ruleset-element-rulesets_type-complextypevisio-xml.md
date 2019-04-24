---
title: Elemento RuleSet (RuleSets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa um conjunto de regras de validação de diagrama.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318911"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="ed27b-103">Elemento RuleSet (RuleSets_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ed27b-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ed27b-104">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="ed27b-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed27b-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="ed27b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed27b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ed27b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ed27b-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="ed27b-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ed27b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ed27b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ed27b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed27b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ed27b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ed27b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ed27b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ed27b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ed27b-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="ed27b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ed27b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="ed27b-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ed27b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ed27b-114">Elements and attributes</span></span>

<span data-ttu-id="ed27b-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ed27b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ed27b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ed27b-116">Parent elements</span></span>

|<span data-ttu-id="ed27b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed27b-117">**Element**</span></span>|<span data-ttu-id="ed27b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ed27b-118">**Type**</span></span>|<span data-ttu-id="ed27b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ed27b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ed27b-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="ed27b-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ed27b-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="ed27b-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ed27b-122">Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="ed27b-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed27b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ed27b-123">Child elements</span></span>

|<span data-ttu-id="ed27b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed27b-124">**Element**</span></span>|<span data-ttu-id="ed27b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ed27b-125">**Type**</span></span>|<span data-ttu-id="ed27b-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ed27b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ed27b-127">Rule</span><span class="sxs-lookup"><span data-stu-id="ed27b-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ed27b-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="ed27b-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ed27b-129">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="ed27b-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="ed27b-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="ed27b-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ed27b-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="ed27b-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ed27b-132">Especifica as propriedades do conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="ed27b-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ed27b-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed27b-133">Attributes</span></span>

|<span data-ttu-id="ed27b-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ed27b-134">**Attribute**</span></span>|<span data-ttu-id="ed27b-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ed27b-135">**Type**</span></span>|<span data-ttu-id="ed27b-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ed27b-136">**Required**</span></span>|<span data-ttu-id="ed27b-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ed27b-137">**Description**</span></span>|<span data-ttu-id="ed27b-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ed27b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed27b-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed27b-139">Description</span></span>  <br/> |<span data-ttu-id="ed27b-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ed27b-140">xsd:string</span></span>  <br/> |<span data-ttu-id="ed27b-141">opcional</span><span class="sxs-lookup"><span data-stu-id="ed27b-141">optional</span></span>  <br/> |<span data-ttu-id="ed27b-142">Especifica a descrição que aparece na interface do usuário para o conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="ed27b-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="ed27b-143">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ed27b-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="ed27b-144">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ed27b-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ed27b-145">Habilitado</span><span class="sxs-lookup"><span data-stu-id="ed27b-145">Enabled</span></span>  <br/> |<span data-ttu-id="ed27b-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ed27b-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ed27b-147">opcional</span><span class="sxs-lookup"><span data-stu-id="ed27b-147">optional</span></span>  <br/> |<span data-ttu-id="ed27b-148">Especifica se as regras no conjunto de regras de validação especificado são verificadas quando a validação é disparada para o documento atual.</span><span class="sxs-lookup"><span data-stu-id="ed27b-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="ed27b-149">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="ed27b-149">Default is True.</span></span>  <br/> |<span data-ttu-id="ed27b-150">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ed27b-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ed27b-151">ID</span><span class="sxs-lookup"><span data-stu-id="ed27b-151">ID</span></span>  <br/> |<span data-ttu-id="ed27b-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ed27b-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ed27b-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ed27b-153">required</span></span>  <br/> |<span data-ttu-id="ed27b-154">Especifica o identificador exclusivo do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="ed27b-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="ed27b-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ed27b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ed27b-156">Nome</span><span class="sxs-lookup"><span data-stu-id="ed27b-156">Name</span></span>  <br/> |<span data-ttu-id="ed27b-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ed27b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ed27b-158">opcional</span><span class="sxs-lookup"><span data-stu-id="ed27b-158">optional</span></span>  <br/> |<span data-ttu-id="ed27b-159">Especifica o nome local do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="ed27b-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="ed27b-160">O padrão é o valor do atributo nameu.</span><span class="sxs-lookup"><span data-stu-id="ed27b-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="ed27b-161">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ed27b-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ed27b-162">NameU</span><span class="sxs-lookup"><span data-stu-id="ed27b-162">NameU</span></span>  <br/> |<span data-ttu-id="ed27b-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ed27b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ed27b-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ed27b-164">required</span></span>  <br/> |<span data-ttu-id="ed27b-165">Especifica o nome universal do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="ed27b-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="ed27b-166">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ed27b-166">Values of the xsd:string type.</span></span>  <br/> |
   

