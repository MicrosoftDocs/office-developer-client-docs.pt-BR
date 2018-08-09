---
title: Elemento de regra (RuleSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772803"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="763d4-103">Elemento de regra (RuleSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="763d4-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="763d4-104">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="763d4-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="763d4-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="763d4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="763d4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="763d4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="763d4-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="763d4-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="763d4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="763d4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="763d4-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="763d4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="763d4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="763d4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="763d4-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="763d4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="763d4-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="763d4-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="763d4-113">Definição</span><span class="sxs-lookup"><span data-stu-id="763d4-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="763d4-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="763d4-114">Elements and attributes</span></span>

<span data-ttu-id="763d4-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="763d4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="763d4-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="763d4-116">Parent elements</span></span>

|<span data-ttu-id="763d4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="763d4-117">**Element**</span></span>|<span data-ttu-id="763d4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="763d4-118">**Type**</span></span>|<span data-ttu-id="763d4-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="763d4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="763d4-120">Conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="763d4-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="763d4-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="763d4-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="763d4-122">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="763d4-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="763d4-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="763d4-123">Child elements</span></span>

|<span data-ttu-id="763d4-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="763d4-124">**Element**</span></span>|<span data-ttu-id="763d4-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="763d4-125">**Type**</span></span>|<span data-ttu-id="763d4-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="763d4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="763d4-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="763d4-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="763d4-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="763d4-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="763d4-129">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="763d4-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="763d4-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="763d4-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="763d4-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="763d4-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="763d4-132">Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="763d4-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="763d4-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="763d4-133">Attributes</span></span>

|<span data-ttu-id="763d4-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="763d4-134">**Attribute**</span></span>|<span data-ttu-id="763d4-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="763d4-135">**Type**</span></span>|<span data-ttu-id="763d4-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="763d4-136">**Required**</span></span>|<span data-ttu-id="763d4-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="763d4-137">**Description**</span></span>|<span data-ttu-id="763d4-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="763d4-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="763d4-139">Category</span><span class="sxs-lookup"><span data-stu-id="763d4-139">Category</span></span>  <br/> |<span data-ttu-id="763d4-140">XSD: String</span><span class="sxs-lookup"><span data-stu-id="763d4-140">xsd:string</span></span>  <br/> |<span data-ttu-id="763d4-141">opcional</span><span class="sxs-lookup"><span data-stu-id="763d4-141">optional</span></span>  <br/> |<span data-ttu-id="763d4-142">Especifica o texto exibido na coluna **categoria** da janela questões.</span><span class="sxs-lookup"><span data-stu-id="763d4-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="763d4-143">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="763d4-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="763d4-144">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="763d4-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="763d4-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="763d4-145">Description</span></span>  <br/> |<span data-ttu-id="763d4-146">XSD: String</span><span class="sxs-lookup"><span data-stu-id="763d4-146">xsd:string</span></span>  <br/> |<span data-ttu-id="763d4-147">opcional</span><span class="sxs-lookup"><span data-stu-id="763d4-147">optional</span></span>  <br/> |<span data-ttu-id="763d4-148">Especifica a descrição da regra de validação que aparece na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="763d4-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="763d4-149">O padrão é "Desconhecido".</span><span class="sxs-lookup"><span data-stu-id="763d4-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="763d4-150">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="763d4-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="763d4-151">ID</span><span class="sxs-lookup"><span data-stu-id="763d4-151">ID</span></span>  <br/> |<span data-ttu-id="763d4-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="763d4-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="763d4-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="763d4-153">required</span></span>  <br/> |<span data-ttu-id="763d4-154">Especifica o identificador exclusivo para a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="763d4-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="763d4-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="763d4-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="763d4-156">Ignorado</span><span class="sxs-lookup"><span data-stu-id="763d4-156">Ignored</span></span>  <br/> |<span data-ttu-id="763d4-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="763d4-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="763d4-158">opcional</span><span class="sxs-lookup"><span data-stu-id="763d4-158">optional</span></span>  <br/> |<span data-ttu-id="763d4-159">Especifica se a regra de validação no momento é ignorada.</span><span class="sxs-lookup"><span data-stu-id="763d4-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="763d4-160">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="763d4-160">Default is False.</span></span>  <br/> |<span data-ttu-id="763d4-161">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="763d4-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="763d4-162">NameU</span><span class="sxs-lookup"><span data-stu-id="763d4-162">NameU</span></span>  <br/> |<span data-ttu-id="763d4-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="763d4-163">xsd:string</span></span>  <br/> |<span data-ttu-id="763d4-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="763d4-164">required</span></span>  <br/> |<span data-ttu-id="763d4-165">Especifica o nome universal da regra de validação.</span><span class="sxs-lookup"><span data-stu-id="763d4-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="763d4-166">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="763d4-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="763d4-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="763d4-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="763d4-168">XSD:int</span><span class="sxs-lookup"><span data-stu-id="763d4-168">xsd:int</span></span>  <br/> |<span data-ttu-id="763d4-169">opcional</span><span class="sxs-lookup"><span data-stu-id="763d4-169">optional</span></span>  <br/> |<span data-ttu-id="763d4-170">Especifica o tipo de objeto ao qual se aplica a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="763d4-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="763d4-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="763d4-171">Values of the xsd:int type.</span></span>  <br/> |
   
