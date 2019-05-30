---
title: Elemento Issue (Issues_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa um único problema de validação no documento.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541124"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="8473e-103">Elemento Issue (Issues_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="8473e-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8473e-104">Representa um único problema de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="8473e-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8473e-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="8473e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8473e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8473e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8473e-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8473e-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8473e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8473e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8473e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8473e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8473e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8473e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8473e-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8473e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8473e-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="8473e-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8473e-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8473e-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8473e-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8473e-114">Elements and attributes</span></span>

<span data-ttu-id="8473e-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8473e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8473e-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8473e-116">Parent elements</span></span>

|<span data-ttu-id="8473e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8473e-117">**Element**</span></span>|<span data-ttu-id="8473e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8473e-118">**Type**</span></span>|<span data-ttu-id="8473e-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8473e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8473e-120">Issues</span><span class="sxs-lookup"><span data-stu-id="8473e-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8473e-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="8473e-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8473e-122">Contém todos os elementos **Issue** do documento.</span><span class="sxs-lookup"><span data-stu-id="8473e-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8473e-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8473e-123">Child elements</span></span>

|<span data-ttu-id="8473e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8473e-124">**Element**</span></span>|<span data-ttu-id="8473e-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8473e-125">**Type**</span></span>|<span data-ttu-id="8473e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8473e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8473e-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="8473e-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8473e-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8473e-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8473e-129">Dependendo do destino do problema de validação pai, especifica a página ou a página e a forma, associadas ao problema de validação pai.</span><span class="sxs-lookup"><span data-stu-id="8473e-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="8473e-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="8473e-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8473e-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8473e-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8473e-132">Especifica informações sobre a regra de validação à qual o problema de validação pai pertence.</span><span class="sxs-lookup"><span data-stu-id="8473e-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8473e-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="8473e-133">Attributes</span></span>

|<span data-ttu-id="8473e-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8473e-134">**Attribute**</span></span>|<span data-ttu-id="8473e-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8473e-135">**Type**</span></span>|<span data-ttu-id="8473e-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8473e-136">**Required**</span></span>|<span data-ttu-id="8473e-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8473e-137">**Description**</span></span>|<span data-ttu-id="8473e-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8473e-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8473e-139">ID</span><span class="sxs-lookup"><span data-stu-id="8473e-139">ID</span></span>  <br/> |<span data-ttu-id="8473e-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8473e-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8473e-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8473e-141">required</span></span>  <br/> |<span data-ttu-id="8473e-142">Especifica o identificador exclusivo do problema de validação.</span><span class="sxs-lookup"><span data-stu-id="8473e-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="8473e-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8473e-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8473e-144">Ignorado</span><span class="sxs-lookup"><span data-stu-id="8473e-144">Ignored</span></span>  <br/> |<span data-ttu-id="8473e-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8473e-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8473e-146">opcional</span><span class="sxs-lookup"><span data-stu-id="8473e-146">optional</span></span>  <br/> |<span data-ttu-id="8473e-147">Especifica informações sobre a regra de validação à qual o problema de validação pai pertence.</span><span class="sxs-lookup"><span data-stu-id="8473e-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="8473e-148">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8473e-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

