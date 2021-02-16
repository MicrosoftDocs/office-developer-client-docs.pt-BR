---
title: Elemento RuleInfo (Issue_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica informações sobre a regra de validação à que pertence a validação pai.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541684"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="87ee9-103">Elemento RuleInfo (Issue_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="87ee9-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="87ee9-104">Especifica informações sobre a regra de validação à que pertence a validação pai.</span><span class="sxs-lookup"><span data-stu-id="87ee9-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87ee9-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="87ee9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87ee9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="87ee9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87ee9-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="87ee9-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87ee9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87ee9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87ee9-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="87ee9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87ee9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87ee9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87ee9-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="87ee9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87ee9-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="87ee9-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87ee9-113">Definição</span><span class="sxs-lookup"><span data-stu-id="87ee9-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87ee9-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="87ee9-114">Elements and attributes</span></span>

<span data-ttu-id="87ee9-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="87ee9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87ee9-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="87ee9-116">Parent elements</span></span>

|<span data-ttu-id="87ee9-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="87ee9-117">**Element**</span></span>|<span data-ttu-id="87ee9-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87ee9-118">**Type**</span></span>|<span data-ttu-id="87ee9-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87ee9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87ee9-120">Problema</span><span class="sxs-lookup"><span data-stu-id="87ee9-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87ee9-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="87ee9-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87ee9-122">Representa uma única questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="87ee9-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87ee9-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="87ee9-123">Child elements</span></span>

<span data-ttu-id="87ee9-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="87ee9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87ee9-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="87ee9-125">Attributes</span></span>

|<span data-ttu-id="87ee9-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="87ee9-126">**Attribute**</span></span>|<span data-ttu-id="87ee9-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87ee9-127">**Type**</span></span>|<span data-ttu-id="87ee9-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="87ee9-128">**Required**</span></span>|<span data-ttu-id="87ee9-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87ee9-129">**Description**</span></span>|<span data-ttu-id="87ee9-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="87ee9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87ee9-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="87ee9-131">RuleID</span></span>  <br/> |<span data-ttu-id="87ee9-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="87ee9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87ee9-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="87ee9-133">required</span></span>  <br/> |<span data-ttu-id="87ee9-134">Especifica o identificador exclusivo da regra de validação à que pertence o problema pai.</span><span class="sxs-lookup"><span data-stu-id="87ee9-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="87ee9-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="87ee9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="87ee9-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="87ee9-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="87ee9-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="87ee9-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87ee9-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="87ee9-138">required</span></span>  <br/> |<span data-ttu-id="87ee9-139">Especifica o identificador exclusivo do conjunto de regras de validação ao que o problema pai pertence.</span><span class="sxs-lookup"><span data-stu-id="87ee9-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="87ee9-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="87ee9-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

