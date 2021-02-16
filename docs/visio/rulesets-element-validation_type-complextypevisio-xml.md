---
title: Elemento RuleSets (Validation_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Inclui um elemento RuleSet para cada conjunto de regras de validação no documento.
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541572"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="9c35c-103">Elemento RuleSets (Validation_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="9c35c-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9c35c-104">Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="9c35c-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9c35c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9c35c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c35c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9c35c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9c35c-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="9c35c-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9c35c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c35c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9c35c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9c35c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9c35c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9c35c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9c35c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9c35c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9c35c-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="9c35c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c35c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9c35c-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c35c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9c35c-114">Elements and attributes</span></span>

<span data-ttu-id="9c35c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9c35c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9c35c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9c35c-116">Parent elements</span></span>

|<span data-ttu-id="9c35c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c35c-117">**Element**</span></span>|<span data-ttu-id="9c35c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c35c-118">**Type**</span></span>|<span data-ttu-id="9c35c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c35c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c35c-120">Validation</span><span class="sxs-lookup"><span data-stu-id="9c35c-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="9c35c-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="9c35c-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c35c-122">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="9c35c-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c35c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9c35c-123">Child elements</span></span>

|<span data-ttu-id="9c35c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c35c-124">**Element**</span></span>|<span data-ttu-id="9c35c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c35c-125">**Type**</span></span>|<span data-ttu-id="9c35c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c35c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c35c-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="9c35c-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c35c-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9c35c-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c35c-129">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="9c35c-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9c35c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c35c-130">Attributes</span></span>

<span data-ttu-id="9c35c-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9c35c-131">None.</span></span>
  

