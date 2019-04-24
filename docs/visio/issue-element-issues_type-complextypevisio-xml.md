---
title: Elemento Issue (Issues_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa um único problema de validação no documento.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317903"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="932a6-103">Elemento Issue (Issues_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="932a6-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="932a6-104">Representa um único problema de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="932a6-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="932a6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="932a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="932a6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="932a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="932a6-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="932a6-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="932a6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="932a6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="932a6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="932a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="932a6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="932a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="932a6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="932a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="932a6-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="932a6-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="932a6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="932a6-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="932a6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="932a6-114">Elements and attributes</span></span>

<span data-ttu-id="932a6-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="932a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="932a6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="932a6-116">Parent elements</span></span>

|<span data-ttu-id="932a6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="932a6-117">**Element**</span></span>|<span data-ttu-id="932a6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="932a6-118">**Type**</span></span>|<span data-ttu-id="932a6-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="932a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="932a6-120">Issues</span><span class="sxs-lookup"><span data-stu-id="932a6-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="932a6-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="932a6-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932a6-122">Contém todos os elementos **Issue** do documento.</span><span class="sxs-lookup"><span data-stu-id="932a6-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="932a6-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="932a6-123">Child elements</span></span>

|<span data-ttu-id="932a6-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="932a6-124">**Element**</span></span>|<span data-ttu-id="932a6-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="932a6-125">**Type**</span></span>|<span data-ttu-id="932a6-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="932a6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="932a6-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="932a6-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="932a6-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="932a6-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932a6-129">Dependendo do destino do problema de validação pai, especifica a página ou a página e a forma, associadas ao problema de validação pai.</span><span class="sxs-lookup"><span data-stu-id="932a6-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="932a6-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="932a6-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="932a6-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="932a6-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932a6-132">Especifica informações sobre a regra de validação à qual o problema de validação pai pertence.</span><span class="sxs-lookup"><span data-stu-id="932a6-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="932a6-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="932a6-133">Attributes</span></span>

|<span data-ttu-id="932a6-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="932a6-134">**Attribute**</span></span>|<span data-ttu-id="932a6-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="932a6-135">**Type**</span></span>|<span data-ttu-id="932a6-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="932a6-136">**Required**</span></span>|<span data-ttu-id="932a6-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="932a6-137">**Description**</span></span>|<span data-ttu-id="932a6-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="932a6-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="932a6-139">ID</span><span class="sxs-lookup"><span data-stu-id="932a6-139">ID</span></span>  <br/> |<span data-ttu-id="932a6-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="932a6-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="932a6-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="932a6-141">required</span></span>  <br/> |<span data-ttu-id="932a6-142">Especifica o identificador exclusivo do problema de validação.</span><span class="sxs-lookup"><span data-stu-id="932a6-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="932a6-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="932a6-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="932a6-144">Ignorado</span><span class="sxs-lookup"><span data-stu-id="932a6-144">Ignored</span></span>  <br/> |<span data-ttu-id="932a6-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="932a6-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="932a6-146">opcional</span><span class="sxs-lookup"><span data-stu-id="932a6-146">optional</span></span>  <br/> |<span data-ttu-id="932a6-147">Especifica informações sobre a regra de validação à qual o problema de validação pai pertence.</span><span class="sxs-lookup"><span data-stu-id="932a6-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="932a6-148">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="932a6-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

