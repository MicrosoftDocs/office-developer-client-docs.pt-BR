---
title: Elemento IssueTarget (Issue_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Dependendo do destino do problema de validação pai, especifica a página ou a página e a forma, associadas ao problema de validação pai. Se o destino do problema de validação pai for um documento, IssueTarget especificará nenhuma página nem uma forma.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542951"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="85cb5-104">Elemento IssueTarget (Issue_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="85cb5-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="85cb5-105">Dependendo do destino do problema de validação pai, especifica a página ou a página e a forma, associadas ao problema de validação pai.</span><span class="sxs-lookup"><span data-stu-id="85cb5-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="85cb5-106">Se o destino do problema de validação pai for um documento, **IssueTarget** especificará nenhuma página nem uma forma.</span><span class="sxs-lookup"><span data-stu-id="85cb5-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="85cb5-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="85cb5-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85cb5-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="85cb5-108">**Element type**</span></span> <br/> |[<span data-ttu-id="85cb5-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="85cb5-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="85cb5-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85cb5-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="85cb5-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85cb5-111">**Schema file**</span></span> <br/> |<span data-ttu-id="85cb5-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="85cb5-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="85cb5-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="85cb5-113">**Document parts**</span></span> <br/> |<span data-ttu-id="85cb5-114">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="85cb5-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85cb5-115">Definição</span><span class="sxs-lookup"><span data-stu-id="85cb5-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85cb5-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="85cb5-116">Elements and attributes</span></span>

<span data-ttu-id="85cb5-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="85cb5-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="85cb5-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="85cb5-118">Parent elements</span></span>

|<span data-ttu-id="85cb5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85cb5-119">**Element**</span></span>|<span data-ttu-id="85cb5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85cb5-120">**Type**</span></span>|<span data-ttu-id="85cb5-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85cb5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85cb5-122">Problema</span><span class="sxs-lookup"><span data-stu-id="85cb5-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85cb5-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="85cb5-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85cb5-124">Representa um único problema de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="85cb5-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85cb5-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="85cb5-125">Child elements</span></span>

<span data-ttu-id="85cb5-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="85cb5-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85cb5-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="85cb5-127">Attributes</span></span>

|<span data-ttu-id="85cb5-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="85cb5-128">**Attribute**</span></span>|<span data-ttu-id="85cb5-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85cb5-129">**Type**</span></span>|<span data-ttu-id="85cb5-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="85cb5-130">**Required**</span></span>|<span data-ttu-id="85cb5-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85cb5-131">**Description**</span></span>|<span data-ttu-id="85cb5-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="85cb5-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85cb5-133">PageID</span><span class="sxs-lookup"><span data-stu-id="85cb5-133">PageID</span></span>  <br/> |<span data-ttu-id="85cb5-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85cb5-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85cb5-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="85cb5-135">required</span></span>  <br/> |<span data-ttu-id="85cb5-136">Especifica o identificador exclusivo da página associada ao problema de validação pai.</span><span class="sxs-lookup"><span data-stu-id="85cb5-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="85cb5-137">Se o destino for o documento, o valor PageId poderá ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="85cb5-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="85cb5-138">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85cb5-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85cb5-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="85cb5-139">ShapeID</span></span>  <br/> |<span data-ttu-id="85cb5-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85cb5-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85cb5-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="85cb5-141">required</span></span>  <br/> |<span data-ttu-id="85cb5-142">Especifica o identificador exclusivo da forma associada ao problema de validação pai.</span><span class="sxs-lookup"><span data-stu-id="85cb5-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="85cb5-143">Se o destino for o documento ou uma página, o valor ShapeID poderá ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="85cb5-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="85cb5-144">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85cb5-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

