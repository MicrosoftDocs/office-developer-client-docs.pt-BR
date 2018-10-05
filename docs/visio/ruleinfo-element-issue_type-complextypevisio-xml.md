---
title: Elemento RuleInfo (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica informações sobre a regra de validação que aborde o problema de validação do pai.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394745"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="7fcb7-103">Elemento RuleInfo (Issue_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7fcb7-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7fcb7-104">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fcb7-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="7fcb7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fcb7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7fcb7-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="7fcb7-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7fcb7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7fcb7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7fcb7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7fcb7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7fcb7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7fcb7-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="7fcb7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fcb7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7fcb7-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7fcb7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7fcb7-114">Elements and attributes</span></span>

<span data-ttu-id="7fcb7-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7fcb7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7fcb7-116">Parent elements</span></span>

|<span data-ttu-id="7fcb7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-117">**Element**</span></span>|<span data-ttu-id="7fcb7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-118">**Type**</span></span>|<span data-ttu-id="7fcb7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7fcb7-120">Problema</span><span class="sxs-lookup"><span data-stu-id="7fcb7-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7fcb7-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="7fcb7-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7fcb7-122">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fcb7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7fcb7-123">Child elements</span></span>

<span data-ttu-id="7fcb7-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fcb7-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fcb7-125">Attributes</span></span>

|<span data-ttu-id="7fcb7-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-126">**Attribute**</span></span>|<span data-ttu-id="7fcb7-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-127">**Type**</span></span>|<span data-ttu-id="7fcb7-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-128">**Required**</span></span>|<span data-ttu-id="7fcb7-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-129">**Description**</span></span>|<span data-ttu-id="7fcb7-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7fcb7-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="7fcb7-131">RuleID</span></span>  <br/> |<span data-ttu-id="7fcb7-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fcb7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fcb7-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7fcb7-133">required</span></span>  <br/> |<span data-ttu-id="7fcb7-134">Especifica o identificador exclusivo da regra de validação que aborde o problema pai.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="7fcb7-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fcb7-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="7fcb7-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="7fcb7-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fcb7-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fcb7-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7fcb7-138">required</span></span>  <br/> |<span data-ttu-id="7fcb7-139">Especifica o identificador exclusivo do conjunto de regras de validação que aborde o problema pai.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="7fcb7-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

