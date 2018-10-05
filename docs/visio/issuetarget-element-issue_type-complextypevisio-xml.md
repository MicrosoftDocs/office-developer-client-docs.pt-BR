---
title: Elemento IssueTarget (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai. Se o destino da questão de validação do pai for um documento, IssueTarget especifica nem uma página nem uma forma.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385358"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="9d031-104">Elemento IssueTarget (Issue_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9d031-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9d031-105">Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="9d031-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="9d031-106">Se o destino da questão de validação do pai for um documento, **IssueTarget** especifica nem uma página nem uma forma.</span><span class="sxs-lookup"><span data-stu-id="9d031-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9d031-107">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="9d031-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d031-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9d031-108">**Element type**</span></span> <br/> |[<span data-ttu-id="9d031-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="9d031-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9d031-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d031-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9d031-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d031-111">**Schema file**</span></span> <br/> |<span data-ttu-id="9d031-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9d031-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9d031-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9d031-113">**Document parts**</span></span> <br/> |<span data-ttu-id="9d031-114">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="9d031-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d031-115">Definição</span><span class="sxs-lookup"><span data-stu-id="9d031-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d031-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9d031-116">Elements and attributes</span></span>

<span data-ttu-id="9d031-117">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9d031-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d031-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9d031-118">Parent elements</span></span>

|<span data-ttu-id="9d031-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d031-119">**Element**</span></span>|<span data-ttu-id="9d031-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d031-120">**Type**</span></span>|<span data-ttu-id="9d031-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d031-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d031-122">Problema</span><span class="sxs-lookup"><span data-stu-id="9d031-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d031-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="9d031-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d031-124">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="9d031-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d031-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d031-125">Child elements</span></span>

<span data-ttu-id="9d031-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9d031-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d031-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d031-127">Attributes</span></span>

|<span data-ttu-id="9d031-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9d031-128">**Attribute**</span></span>|<span data-ttu-id="9d031-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d031-129">**Type**</span></span>|<span data-ttu-id="9d031-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9d031-130">**Required**</span></span>|<span data-ttu-id="9d031-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d031-131">**Description**</span></span>|<span data-ttu-id="9d031-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9d031-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d031-133">PageID</span><span class="sxs-lookup"><span data-stu-id="9d031-133">PageID</span></span>  <br/> |<span data-ttu-id="9d031-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9d031-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9d031-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d031-135">required</span></span>  <br/> |<span data-ttu-id="9d031-136">Especifica o identificador exclusivo da página que está associado a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="9d031-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="9d031-137">Se o destino for o documento, o valor de PageID pode ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9d031-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="9d031-138">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9d031-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9d031-139">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="9d031-139">ShapeID</span></span>  <br/> |<span data-ttu-id="9d031-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9d031-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9d031-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d031-141">required</span></span>  <br/> |<span data-ttu-id="9d031-142">Especifica o identificador exclusivo da forma que está associado com a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="9d031-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="9d031-143">Se o destino for um documento ou uma página, o valor de identificação da forma pode ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9d031-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="9d031-144">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9d031-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

