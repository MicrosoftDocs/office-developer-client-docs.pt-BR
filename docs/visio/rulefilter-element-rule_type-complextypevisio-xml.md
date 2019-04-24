---
title: Elemento RuleFilter (Rule_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349382"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="4fe5b-103">Elemento RuleFilter (Rule_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4fe5b-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4fe5b-104">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fe5b-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="4fe5b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fe5b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4fe5b-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="4fe5b-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4fe5b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4fe5b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4fe5b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4fe5b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4fe5b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4fe5b-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="4fe5b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fe5b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="4fe5b-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4fe5b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4fe5b-114">Elements and attributes</span></span>

<span data-ttu-id="4fe5b-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4fe5b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4fe5b-116">Parent elements</span></span>

|<span data-ttu-id="4fe5b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-117">**Element**</span></span>|<span data-ttu-id="4fe5b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-118">**Type**</span></span>|<span data-ttu-id="4fe5b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4fe5b-120">Rule</span><span class="sxs-lookup"><span data-stu-id="4fe5b-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4fe5b-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="4fe5b-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4fe5b-122">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4fe5b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4fe5b-123">Child elements</span></span>

<span data-ttu-id="4fe5b-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fe5b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="4fe5b-125">Attributes</span></span>

|<span data-ttu-id="4fe5b-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-126">**Attribute**</span></span>|<span data-ttu-id="4fe5b-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-127">**Type**</span></span>|<span data-ttu-id="4fe5b-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-128">**Required**</span></span>|<span data-ttu-id="4fe5b-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-129">**Description**</span></span>|<span data-ttu-id="4fe5b-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4fe5b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4fe5b-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="4fe5b-131">Formula</span></span>  <br/> |<span data-ttu-id="4fe5b-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4fe5b-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4fe5b-133">opcional</span><span class="sxs-lookup"><span data-stu-id="4fe5b-133">optional</span></span>  <br/> |<span data-ttu-id="4fe5b-134">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="4fe5b-135">Valores da cadeia de caracteres xsd:.</span><span class="sxs-lookup"><span data-stu-id="4fe5b-135">Values of the xsd:string.</span></span>  <br/> |
   

