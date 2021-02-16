---
title: Elemento Issue (Issues_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa uma única questão de validação no documento.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541124"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="85add-103">Elemento Issue (Issues_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="85add-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="85add-104">Representa uma única questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="85add-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85add-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="85add-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85add-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="85add-106">**Element type**</span></span> <br/> |[<span data-ttu-id="85add-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="85add-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="85add-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85add-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="85add-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85add-109">**Schema file**</span></span> <br/> |<span data-ttu-id="85add-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="85add-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="85add-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="85add-111">**Document parts**</span></span> <br/> |<span data-ttu-id="85add-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="85add-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85add-113">Definição</span><span class="sxs-lookup"><span data-stu-id="85add-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85add-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="85add-114">Elements and attributes</span></span>

<span data-ttu-id="85add-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="85add-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="85add-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="85add-116">Parent elements</span></span>

|<span data-ttu-id="85add-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85add-117">**Element**</span></span>|<span data-ttu-id="85add-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85add-118">**Type**</span></span>|<span data-ttu-id="85add-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85add-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85add-120">Issues</span><span class="sxs-lookup"><span data-stu-id="85add-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85add-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="85add-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85add-122">Contém todos os **elementos Issue** do documento.</span><span class="sxs-lookup"><span data-stu-id="85add-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85add-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="85add-123">Child elements</span></span>

|<span data-ttu-id="85add-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85add-124">**Element**</span></span>|<span data-ttu-id="85add-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85add-125">**Type**</span></span>|<span data-ttu-id="85add-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85add-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85add-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="85add-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85add-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="85add-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85add-129">Dependendo do destino da questão de validação pai, especifica a página ou a página e a forma, associadas à questão de validação pai.</span><span class="sxs-lookup"><span data-stu-id="85add-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="85add-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="85add-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85add-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="85add-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85add-132">Especifica informações sobre a regra de validação à que pertence a validação pai.</span><span class="sxs-lookup"><span data-stu-id="85add-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="85add-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="85add-133">Attributes</span></span>

|<span data-ttu-id="85add-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="85add-134">**Attribute**</span></span>|<span data-ttu-id="85add-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85add-135">**Type**</span></span>|<span data-ttu-id="85add-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="85add-136">**Required**</span></span>|<span data-ttu-id="85add-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85add-137">**Description**</span></span>|<span data-ttu-id="85add-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="85add-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85add-139">ID</span><span class="sxs-lookup"><span data-stu-id="85add-139">ID</span></span>  <br/> |<span data-ttu-id="85add-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85add-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85add-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="85add-141">required</span></span>  <br/> |<span data-ttu-id="85add-142">Especifica o identificador exclusivo da questão de validação.</span><span class="sxs-lookup"><span data-stu-id="85add-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="85add-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85add-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85add-144">Ignorado</span><span class="sxs-lookup"><span data-stu-id="85add-144">Ignored</span></span>  <br/> |<span data-ttu-id="85add-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="85add-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85add-146">opcional</span><span class="sxs-lookup"><span data-stu-id="85add-146">optional</span></span>  <br/> |<span data-ttu-id="85add-147">Especifica informações sobre a regra de validação à que pertence a validação pai.</span><span class="sxs-lookup"><span data-stu-id="85add-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="85add-148">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="85add-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

