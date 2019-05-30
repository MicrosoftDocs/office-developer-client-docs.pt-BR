---
title: Elemento RuleFilter (Rule_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541677"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="992cb-103">Elemento RuleFilter (Rule_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="992cb-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="992cb-104">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="992cb-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="992cb-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="992cb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="992cb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="992cb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="992cb-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="992cb-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="992cb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="992cb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="992cb-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="992cb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="992cb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="992cb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="992cb-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="992cb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="992cb-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="992cb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="992cb-113">Definição</span><span class="sxs-lookup"><span data-stu-id="992cb-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="992cb-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="992cb-114">Elements and attributes</span></span>

<span data-ttu-id="992cb-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="992cb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="992cb-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="992cb-116">Parent elements</span></span>

|<span data-ttu-id="992cb-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="992cb-117">**Element**</span></span>|<span data-ttu-id="992cb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="992cb-118">**Type**</span></span>|<span data-ttu-id="992cb-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="992cb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="992cb-120">Rule</span><span class="sxs-lookup"><span data-stu-id="992cb-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="992cb-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="992cb-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="992cb-122">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="992cb-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="992cb-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="992cb-123">Child elements</span></span>

<span data-ttu-id="992cb-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="992cb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="992cb-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="992cb-125">Attributes</span></span>

|<span data-ttu-id="992cb-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="992cb-126">**Attribute**</span></span>|<span data-ttu-id="992cb-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="992cb-127">**Type**</span></span>|<span data-ttu-id="992cb-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="992cb-128">**Required**</span></span>|<span data-ttu-id="992cb-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="992cb-129">**Description**</span></span>|<span data-ttu-id="992cb-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="992cb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="992cb-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="992cb-131">Formula</span></span>  <br/> |<span data-ttu-id="992cb-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="992cb-132">xsd:string</span></span>  <br/> |<span data-ttu-id="992cb-133">opcional</span><span class="sxs-lookup"><span data-stu-id="992cb-133">optional</span></span>  <br/> |<span data-ttu-id="992cb-134">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="992cb-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="992cb-135">Valores da cadeia de caracteres xsd:.</span><span class="sxs-lookup"><span data-stu-id="992cb-135">Values of the xsd:string.</span></span>  <br/> |
   

