---
title: Elemento IssueTarget (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai. Se o destino da questão de validação do pai for um documento, IssueTarget especifica nem uma página nem uma forma.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772142"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="daa62-104">Elemento IssueTarget (Issue_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="daa62-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="daa62-105">Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="daa62-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="daa62-106">Se o destino da questão de validação do pai for um documento, **IssueTarget** especifica nem uma página nem uma forma.</span><span class="sxs-lookup"><span data-stu-id="daa62-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="daa62-107">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="daa62-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daa62-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="daa62-108">**Element type**</span></span> <br/> |[<span data-ttu-id="daa62-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="daa62-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="daa62-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="daa62-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="daa62-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="daa62-111">**Schema file**</span></span> <br/> |<span data-ttu-id="daa62-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="daa62-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="daa62-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="daa62-113">**Document parts**</span></span> <br/> |<span data-ttu-id="daa62-114">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="daa62-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="daa62-115">Definição</span><span class="sxs-lookup"><span data-stu-id="daa62-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="daa62-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="daa62-116">Elements and attributes</span></span>

<span data-ttu-id="daa62-117">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="daa62-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="daa62-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="daa62-118">Parent elements</span></span>

|<span data-ttu-id="daa62-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="daa62-119">**Element**</span></span>|<span data-ttu-id="daa62-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="daa62-120">**Type**</span></span>|<span data-ttu-id="daa62-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="daa62-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="daa62-122">Problema</span><span class="sxs-lookup"><span data-stu-id="daa62-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="daa62-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="daa62-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="daa62-124">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="daa62-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="daa62-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="daa62-125">Child elements</span></span>

<span data-ttu-id="daa62-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="daa62-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="daa62-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="daa62-127">Attributes</span></span>

|<span data-ttu-id="daa62-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="daa62-128">**Attribute**</span></span>|<span data-ttu-id="daa62-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="daa62-129">**Type**</span></span>|<span data-ttu-id="daa62-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="daa62-130">**Required**</span></span>|<span data-ttu-id="daa62-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="daa62-131">**Description**</span></span>|<span data-ttu-id="daa62-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="daa62-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="daa62-133">PageID</span><span class="sxs-lookup"><span data-stu-id="daa62-133">PageID</span></span>  <br/> |<span data-ttu-id="daa62-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="daa62-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="daa62-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="daa62-135">required</span></span>  <br/> |<span data-ttu-id="daa62-136">Especifica o identificador exclusivo da página que está associado a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="daa62-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="daa62-137">Se o destino for o documento, o valor de PageID pode ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="daa62-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="daa62-138">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="daa62-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="daa62-139">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="daa62-139">ShapeID</span></span>  <br/> |<span data-ttu-id="daa62-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="daa62-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="daa62-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="daa62-141">required</span></span>  <br/> |<span data-ttu-id="daa62-142">Especifica o identificador exclusivo da forma que está associado com a questão de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="daa62-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="daa62-143">Se o destino for um documento ou uma página, o valor de identificação da forma pode ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="daa62-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="daa62-144">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="daa62-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

