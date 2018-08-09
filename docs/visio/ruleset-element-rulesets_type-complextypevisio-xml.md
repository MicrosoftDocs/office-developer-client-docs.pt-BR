---
title: Elemento RuleSet (RuleSets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa um conjunto de regras de validação de diagrama.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772823"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="c851e-103">Elemento RuleSet (RuleSets_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c851e-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c851e-104">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="c851e-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c851e-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="c851e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c851e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c851e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c851e-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="c851e-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c851e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c851e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c851e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c851e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c851e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c851e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c851e-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c851e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c851e-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="c851e-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c851e-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c851e-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c851e-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c851e-114">Elements and attributes</span></span>

<span data-ttu-id="c851e-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c851e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c851e-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c851e-116">Parent elements</span></span>

|<span data-ttu-id="c851e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c851e-117">**Element**</span></span>|<span data-ttu-id="c851e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c851e-118">**Type**</span></span>|<span data-ttu-id="c851e-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c851e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c851e-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="c851e-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c851e-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="c851e-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c851e-122">Inclui um elemento **RuleSet** para cada regra de validação definida no documento.</span><span class="sxs-lookup"><span data-stu-id="c851e-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c851e-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c851e-123">Child elements</span></span>

|<span data-ttu-id="c851e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c851e-124">**Element**</span></span>|<span data-ttu-id="c851e-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c851e-125">**Type**</span></span>|<span data-ttu-id="c851e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c851e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c851e-127">Rule</span><span class="sxs-lookup"><span data-stu-id="c851e-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c851e-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="c851e-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c851e-129">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="c851e-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="c851e-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="c851e-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c851e-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="c851e-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c851e-132">Especifica as propriedades de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="c851e-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c851e-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="c851e-133">Attributes</span></span>

|<span data-ttu-id="c851e-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c851e-134">**Attribute**</span></span>|<span data-ttu-id="c851e-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c851e-135">**Type**</span></span>|<span data-ttu-id="c851e-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c851e-136">**Required**</span></span>|<span data-ttu-id="c851e-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c851e-137">**Description**</span></span>|<span data-ttu-id="c851e-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c851e-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c851e-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="c851e-139">Description</span></span>  <br/> |<span data-ttu-id="c851e-140">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c851e-140">xsd:string</span></span>  <br/> |<span data-ttu-id="c851e-141">opcional</span><span class="sxs-lookup"><span data-stu-id="c851e-141">optional</span></span>  <br/> |<span data-ttu-id="c851e-142">Especifica a descrição que aparece na interface do usuário para o conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="c851e-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="c851e-143">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="c851e-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="c851e-144">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c851e-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c851e-145">Habilitado</span><span class="sxs-lookup"><span data-stu-id="c851e-145">Enabled</span></span>  <br/> |<span data-ttu-id="c851e-146">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="c851e-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c851e-147">opcional</span><span class="sxs-lookup"><span data-stu-id="c851e-147">optional</span></span>  <br/> |<span data-ttu-id="c851e-148">Especifica se as regras no conjunto de regras de validação especificado serão verificadas quando a validação é disparada para o documento atual.</span><span class="sxs-lookup"><span data-stu-id="c851e-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="c851e-149">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="c851e-149">Default is True.</span></span>  <br/> |<span data-ttu-id="c851e-150">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c851e-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c851e-151">ID</span><span class="sxs-lookup"><span data-stu-id="c851e-151">ID</span></span>  <br/> |<span data-ttu-id="c851e-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c851e-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c851e-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c851e-153">required</span></span>  <br/> |<span data-ttu-id="c851e-154">Especifica o identificador exclusivo do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="c851e-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="c851e-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c851e-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c851e-156">Nome</span><span class="sxs-lookup"><span data-stu-id="c851e-156">Name</span></span>  <br/> |<span data-ttu-id="c851e-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c851e-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c851e-158">opcional</span><span class="sxs-lookup"><span data-stu-id="c851e-158">optional</span></span>  <br/> |<span data-ttu-id="c851e-159">Especifica o nome local do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="c851e-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="c851e-160">Por padrão, o valor do atributo NameU.</span><span class="sxs-lookup"><span data-stu-id="c851e-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="c851e-161">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c851e-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c851e-162">NameU</span><span class="sxs-lookup"><span data-stu-id="c851e-162">NameU</span></span>  <br/> |<span data-ttu-id="c851e-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c851e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c851e-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c851e-164">required</span></span>  <br/> |<span data-ttu-id="c851e-165">Especifica o nome universal do conjunto de regras de validação.</span><span class="sxs-lookup"><span data-stu-id="c851e-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="c851e-166">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c851e-166">Values of the xsd:string type.</span></span>  <br/> |
   

