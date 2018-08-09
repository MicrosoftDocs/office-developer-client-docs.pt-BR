---
title: Elemento RuleInfo (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica informações sobre a regra de validação que aborde o problema de validação do pai.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772806"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="8ace6-103">Elemento RuleInfo (Issue_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8ace6-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8ace6-104">Especifica informações sobre a regra de validação que aborde o problema de validação do pai.</span><span class="sxs-lookup"><span data-stu-id="8ace6-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ace6-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="8ace6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ace6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8ace6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8ace6-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8ace6-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8ace6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ace6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8ace6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ace6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8ace6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8ace6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8ace6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8ace6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8ace6-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="8ace6-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ace6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8ace6-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ace6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8ace6-114">Elements and attributes</span></span>

<span data-ttu-id="8ace6-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8ace6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8ace6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8ace6-116">Parent elements</span></span>

|<span data-ttu-id="8ace6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8ace6-117">**Element**</span></span>|<span data-ttu-id="8ace6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8ace6-118">**Type**</span></span>|<span data-ttu-id="8ace6-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ace6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ace6-120">Problema</span><span class="sxs-lookup"><span data-stu-id="8ace6-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ace6-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8ace6-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ace6-122">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="8ace6-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ace6-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8ace6-123">Child elements</span></span>

<span data-ttu-id="8ace6-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8ace6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ace6-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ace6-125">Attributes</span></span>

|<span data-ttu-id="8ace6-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8ace6-126">**Attribute**</span></span>|<span data-ttu-id="8ace6-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8ace6-127">**Type**</span></span>|<span data-ttu-id="8ace6-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8ace6-128">**Required**</span></span>|<span data-ttu-id="8ace6-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ace6-129">**Description**</span></span>|<span data-ttu-id="8ace6-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8ace6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8ace6-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="8ace6-131">RuleID</span></span>  <br/> |<span data-ttu-id="8ace6-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ace6-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ace6-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8ace6-133">required</span></span>  <br/> |<span data-ttu-id="8ace6-134">Especifica o identificador exclusivo da regra de validação que aborde o problema pai.</span><span class="sxs-lookup"><span data-stu-id="8ace6-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="8ace6-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ace6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ace6-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="8ace6-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="8ace6-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ace6-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ace6-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8ace6-138">required</span></span>  <br/> |<span data-ttu-id="8ace6-139">Especifica o identificador exclusivo do conjunto de regras de validação que aborde o problema pai.</span><span class="sxs-lookup"><span data-stu-id="8ace6-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="8ace6-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ace6-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

