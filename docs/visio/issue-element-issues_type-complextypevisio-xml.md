---
title: Elemento de problema (Issues_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa uma questão de validação no documento.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772125"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="30199-103">Elemento de problema (Issues_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="30199-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="30199-104">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="30199-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30199-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="30199-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30199-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="30199-106">**Element type**</span></span> <br/> |[<span data-ttu-id="30199-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="30199-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="30199-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30199-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="30199-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="30199-109">**Schema file**</span></span> <br/> |<span data-ttu-id="30199-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="30199-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="30199-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="30199-111">**Document parts**</span></span> <br/> |<span data-ttu-id="30199-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="30199-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30199-113">Definição</span><span class="sxs-lookup"><span data-stu-id="30199-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="30199-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="30199-114">Elements and attributes</span></span>

<span data-ttu-id="30199-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="30199-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="30199-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="30199-116">Parent elements</span></span>

|<span data-ttu-id="30199-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="30199-117">**Element**</span></span>|<span data-ttu-id="30199-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30199-118">**Type**</span></span>|<span data-ttu-id="30199-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30199-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30199-120">Problemas</span><span class="sxs-lookup"><span data-stu-id="30199-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30199-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="30199-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30199-122">Contém todos os elementos de **problema** para o documento.</span><span class="sxs-lookup"><span data-stu-id="30199-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30199-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="30199-123">Child elements</span></span>

|<span data-ttu-id="30199-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="30199-124">**Element**</span></span>|<span data-ttu-id="30199-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30199-125">**Type**</span></span>|<span data-ttu-id="30199-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30199-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30199-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="30199-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30199-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="30199-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30199-129">Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="30199-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="30199-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="30199-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30199-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="30199-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30199-132">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="30199-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="30199-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="30199-133">Attributes</span></span>

|<span data-ttu-id="30199-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="30199-134">**Attribute**</span></span>|<span data-ttu-id="30199-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30199-135">**Type**</span></span>|<span data-ttu-id="30199-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="30199-136">**Required**</span></span>|<span data-ttu-id="30199-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30199-137">**Description**</span></span>|<span data-ttu-id="30199-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="30199-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30199-139">ID</span><span class="sxs-lookup"><span data-stu-id="30199-139">ID</span></span>  <br/> |<span data-ttu-id="30199-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30199-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30199-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="30199-141">required</span></span>  <br/> |<span data-ttu-id="30199-142">Especifica o identificador exclusivo da questão de validação.</span><span class="sxs-lookup"><span data-stu-id="30199-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="30199-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="30199-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30199-144">Ignorado</span><span class="sxs-lookup"><span data-stu-id="30199-144">Ignored</span></span>  <br/> |<span data-ttu-id="30199-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="30199-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30199-146">opcional</span><span class="sxs-lookup"><span data-stu-id="30199-146">optional</span></span>  <br/> |<span data-ttu-id="30199-147">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="30199-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="30199-148">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="30199-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

