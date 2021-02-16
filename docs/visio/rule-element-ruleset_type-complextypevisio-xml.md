---
title: Elemento Rule (RuleSet_Type complexType) (VISio XML)
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
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="7b117-103">Elemento Rule (RuleSet_Type complexType) (VISio XML)</span><span class="sxs-lookup"><span data-stu-id="7b117-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7b117-104">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="7b117-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b117-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="7b117-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b117-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7b117-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7b117-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="7b117-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7b117-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7b117-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7b117-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7b117-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7b117-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7b117-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7b117-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7b117-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7b117-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="7b117-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b117-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7b117-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7b117-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7b117-114">Elements and attributes</span></span>

<span data-ttu-id="7b117-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7b117-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7b117-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7b117-116">Parent elements</span></span>

|<span data-ttu-id="7b117-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b117-117">**Element**</span></span>|<span data-ttu-id="7b117-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b117-118">**Type**</span></span>|<span data-ttu-id="7b117-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b117-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b117-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="7b117-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b117-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="7b117-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b117-122">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="7b117-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b117-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7b117-123">Child elements</span></span>

|<span data-ttu-id="7b117-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b117-124">**Element**</span></span>|<span data-ttu-id="7b117-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b117-125">**Type**</span></span>|<span data-ttu-id="7b117-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b117-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b117-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="7b117-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b117-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="7b117-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b117-129">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="7b117-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="7b117-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="7b117-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b117-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="7b117-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b117-132">Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="7b117-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7b117-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b117-133">Attributes</span></span>

|<span data-ttu-id="7b117-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7b117-134">**Attribute**</span></span>|<span data-ttu-id="7b117-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b117-135">**Type**</span></span>|<span data-ttu-id="7b117-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7b117-136">**Required**</span></span>|<span data-ttu-id="7b117-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b117-137">**Description**</span></span>|<span data-ttu-id="7b117-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7b117-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b117-139">Categoria</span><span class="sxs-lookup"><span data-stu-id="7b117-139">Category</span></span>  <br/> |<span data-ttu-id="7b117-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b117-140">xsd:string</span></span>  <br/> |<span data-ttu-id="7b117-141">opcional</span><span class="sxs-lookup"><span data-stu-id="7b117-141">optional</span></span>  <br/> |<span data-ttu-id="7b117-142">Especifica o texto exibido na coluna **Categoria** da janela Problemas.</span><span class="sxs-lookup"><span data-stu-id="7b117-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="7b117-143">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="7b117-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="7b117-144">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b117-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b117-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b117-145">Description</span></span>  <br/> |<span data-ttu-id="7b117-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b117-146">xsd:string</span></span>  <br/> |<span data-ttu-id="7b117-147">opcional</span><span class="sxs-lookup"><span data-stu-id="7b117-147">optional</span></span>  <br/> |<span data-ttu-id="7b117-148">Especifica a descrição da regra de validação que aparece na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b117-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="7b117-149">O padrão é "Desconhecido".</span><span class="sxs-lookup"><span data-stu-id="7b117-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="7b117-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b117-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b117-151">ID</span><span class="sxs-lookup"><span data-stu-id="7b117-151">ID</span></span>  <br/> |<span data-ttu-id="7b117-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b117-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b117-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7b117-153">required</span></span>  <br/> |<span data-ttu-id="7b117-154">Especifica o identificador exclusivo para a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="7b117-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="7b117-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b117-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b117-156">Ignorado</span><span class="sxs-lookup"><span data-stu-id="7b117-156">Ignored</span></span>  <br/> |<span data-ttu-id="7b117-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7b117-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7b117-158">opcional</span><span class="sxs-lookup"><span data-stu-id="7b117-158">optional</span></span>  <br/> |<span data-ttu-id="7b117-159">Especifica se a regra de validação é ignorada no momento.</span><span class="sxs-lookup"><span data-stu-id="7b117-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="7b117-160">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="7b117-160">Default is False.</span></span>  <br/> |<span data-ttu-id="7b117-161">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7b117-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7b117-162">NameU</span><span class="sxs-lookup"><span data-stu-id="7b117-162">NameU</span></span>  <br/> |<span data-ttu-id="7b117-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b117-163">xsd:string</span></span>  <br/> |<span data-ttu-id="7b117-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7b117-164">required</span></span>  <br/> |<span data-ttu-id="7b117-165">Especifica o nome universal da regra de validação.</span><span class="sxs-lookup"><span data-stu-id="7b117-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="7b117-166">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b117-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b117-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="7b117-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="7b117-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7b117-168">xsd:int</span></span>  <br/> |<span data-ttu-id="7b117-169">opcional</span><span class="sxs-lookup"><span data-stu-id="7b117-169">optional</span></span>  <br/> |<span data-ttu-id="7b117-170">Especifica o tipo de objeto ao qual a regra de validação se aplica.</span><span class="sxs-lookup"><span data-stu-id="7b117-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="7b117-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7b117-171">Values of the xsd:int type.</span></span>  <br/> |
   

