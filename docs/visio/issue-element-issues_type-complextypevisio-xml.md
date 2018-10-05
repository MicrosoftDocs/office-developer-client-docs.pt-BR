---
title: Elemento de problema (Issues_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa uma questão de validação no documento.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389838"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="aad6b-103">Elemento de problema (Issues_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="aad6b-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="aad6b-104">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="aad6b-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aad6b-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="aad6b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aad6b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="aad6b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aad6b-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="aad6b-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aad6b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aad6b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aad6b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aad6b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aad6b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aad6b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aad6b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="aad6b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aad6b-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="aad6b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aad6b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="aad6b-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aad6b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="aad6b-114">Elements and attributes</span></span>

<span data-ttu-id="aad6b-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="aad6b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aad6b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="aad6b-116">Parent elements</span></span>

|<span data-ttu-id="aad6b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aad6b-117">**Element**</span></span>|<span data-ttu-id="aad6b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aad6b-118">**Type**</span></span>|<span data-ttu-id="aad6b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aad6b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aad6b-120">Problemas</span><span class="sxs-lookup"><span data-stu-id="aad6b-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aad6b-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="aad6b-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aad6b-122">Contém todos os elementos de **problema** para o documento.</span><span class="sxs-lookup"><span data-stu-id="aad6b-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aad6b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aad6b-123">Child elements</span></span>

|<span data-ttu-id="aad6b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aad6b-124">**Element**</span></span>|<span data-ttu-id="aad6b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aad6b-125">**Type**</span></span>|<span data-ttu-id="aad6b-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aad6b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aad6b-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="aad6b-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aad6b-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="aad6b-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aad6b-129">Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="aad6b-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="aad6b-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="aad6b-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aad6b-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="aad6b-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aad6b-132">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="aad6b-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aad6b-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="aad6b-133">Attributes</span></span>

|<span data-ttu-id="aad6b-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="aad6b-134">**Attribute**</span></span>|<span data-ttu-id="aad6b-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aad6b-135">**Type**</span></span>|<span data-ttu-id="aad6b-136">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="aad6b-136">**Required**</span></span>|<span data-ttu-id="aad6b-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aad6b-137">**Description**</span></span>|<span data-ttu-id="aad6b-138">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="aad6b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aad6b-139">ID</span><span class="sxs-lookup"><span data-stu-id="aad6b-139">ID</span></span>  <br/> |<span data-ttu-id="aad6b-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aad6b-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aad6b-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="aad6b-141">required</span></span>  <br/> |<span data-ttu-id="aad6b-142">Especifica o identificador exclusivo da questão de validação.</span><span class="sxs-lookup"><span data-stu-id="aad6b-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="aad6b-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aad6b-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aad6b-144">Ignorado</span><span class="sxs-lookup"><span data-stu-id="aad6b-144">Ignored</span></span>  <br/> |<span data-ttu-id="aad6b-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="aad6b-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aad6b-146">opcional</span><span class="sxs-lookup"><span data-stu-id="aad6b-146">optional</span></span>  <br/> |<span data-ttu-id="aad6b-147">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="aad6b-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="aad6b-148">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aad6b-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

