---
title: Elemento Rule (RuleSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541705"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="b2c0c-103">Elemento Rule (RuleSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="b2c0c-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b2c0c-104">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2c0c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="b2c0c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2c0c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b2c0c-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="b2c0c-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b2c0c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b2c0c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b2c0c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b2c0c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b2c0c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b2c0c-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="b2c0c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2c0c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="b2c0c-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2c0c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b2c0c-114">Elements and attributes</span></span>

<span data-ttu-id="b2c0c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b2c0c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b2c0c-116">Parent elements</span></span>

|<span data-ttu-id="b2c0c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-117">**Element**</span></span>|<span data-ttu-id="b2c0c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-118">**Type**</span></span>|<span data-ttu-id="b2c0c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2c0c-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="b2c0c-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2c0c-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="b2c0c-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2c0c-122">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b2c0c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b2c0c-123">Child elements</span></span>

|<span data-ttu-id="b2c0c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-124">**Element**</span></span>|<span data-ttu-id="b2c0c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-125">**Type**</span></span>|<span data-ttu-id="b2c0c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2c0c-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="b2c0c-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2c0c-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="b2c0c-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2c0c-129">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="b2c0c-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="b2c0c-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2c0c-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="b2c0c-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2c0c-132">Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b2c0c-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="b2c0c-133">Attributes</span></span>

|<span data-ttu-id="b2c0c-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-134">**Attribute**</span></span>|<span data-ttu-id="b2c0c-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-135">**Type**</span></span>|<span data-ttu-id="b2c0c-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-136">**Required**</span></span>|<span data-ttu-id="b2c0c-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-137">**Description**</span></span>|<span data-ttu-id="b2c0c-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b2c0c-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2c0c-139">Categoria</span><span class="sxs-lookup"><span data-stu-id="b2c0c-139">Category</span></span>  <br/> |<span data-ttu-id="b2c0c-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b2c0c-140">xsd:string</span></span>  <br/> |<span data-ttu-id="b2c0c-141">opcional</span><span class="sxs-lookup"><span data-stu-id="b2c0c-141">optional</span></span>  <br/> |<span data-ttu-id="b2c0c-142">Especifica o texto exibido na coluna **categoria** da janela questões.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="b2c0c-143">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="b2c0c-144">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2c0c-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2c0c-145">Description</span></span>  <br/> |<span data-ttu-id="b2c0c-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b2c0c-146">xsd:string</span></span>  <br/> |<span data-ttu-id="b2c0c-147">opcional</span><span class="sxs-lookup"><span data-stu-id="b2c0c-147">optional</span></span>  <br/> |<span data-ttu-id="b2c0c-148">Especifica a descrição da regra de validação que aparece na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="b2c0c-149">O padrão é "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b2c0c-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="b2c0c-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2c0c-151">ID</span><span class="sxs-lookup"><span data-stu-id="b2c0c-151">ID</span></span>  <br/> |<span data-ttu-id="b2c0c-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2c0c-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2c0c-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b2c0c-153">required</span></span>  <br/> |<span data-ttu-id="b2c0c-154">Especifica o identificador exclusivo da regra de validação.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="b2c0c-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2c0c-156">Ignorado</span><span class="sxs-lookup"><span data-stu-id="b2c0c-156">Ignored</span></span>  <br/> |<span data-ttu-id="b2c0c-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b2c0c-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b2c0c-158">opcional</span><span class="sxs-lookup"><span data-stu-id="b2c0c-158">optional</span></span>  <br/> |<span data-ttu-id="b2c0c-159">Especifica se a regra de validação é ignorada no momento.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="b2c0c-160">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-160">Default is False.</span></span>  <br/> |<span data-ttu-id="b2c0c-161">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b2c0c-162">NameU</span><span class="sxs-lookup"><span data-stu-id="b2c0c-162">NameU</span></span>  <br/> |<span data-ttu-id="b2c0c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b2c0c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="b2c0c-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b2c0c-164">required</span></span>  <br/> |<span data-ttu-id="b2c0c-165">Especifica o nome universal da regra de validação.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="b2c0c-166">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2c0c-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="b2c0c-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="b2c0c-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b2c0c-168">xsd:int</span></span>  <br/> |<span data-ttu-id="b2c0c-169">opcional</span><span class="sxs-lookup"><span data-stu-id="b2c0c-169">optional</span></span>  <br/> |<span data-ttu-id="b2c0c-170">Especifica o tipo de objeto ao qual a regra de validação se aplica.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="b2c0c-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="b2c0c-171">Values of the xsd:int type.</span></span>  <br/> |
   

