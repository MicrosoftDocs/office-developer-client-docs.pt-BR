---
title: Elemento RuleTest (Rule_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.
ms.openlocfilehash: bb1f0cf9b3f712903f6e45d6d09f96607089f920
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541516"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="70466-103">Elemento RuleTest (Rule_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="70466-103">RuleTest element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="70466-104">Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="70466-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70466-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="70466-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70466-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="70466-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70466-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="70466-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70466-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70466-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70466-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="70466-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70466-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="70466-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70466-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="70466-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70466-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="70466-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70466-113">Definição</span><span class="sxs-lookup"><span data-stu-id="70466-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70466-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="70466-114">Elements and attributes</span></span>

<span data-ttu-id="70466-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="70466-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70466-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="70466-116">Parent elements</span></span>

|<span data-ttu-id="70466-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="70466-117">**Element**</span></span>|<span data-ttu-id="70466-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="70466-118">**Type**</span></span>|<span data-ttu-id="70466-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="70466-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70466-120">Rule</span><span class="sxs-lookup"><span data-stu-id="70466-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70466-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="70466-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70466-122">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="70466-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70466-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="70466-123">Child elements</span></span>

<span data-ttu-id="70466-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="70466-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70466-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="70466-125">Attributes</span></span>

|<span data-ttu-id="70466-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="70466-126">**Attribute**</span></span>|<span data-ttu-id="70466-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="70466-127">**Type**</span></span>|<span data-ttu-id="70466-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="70466-128">**Required**</span></span>|<span data-ttu-id="70466-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="70466-129">**Description**</span></span>|<span data-ttu-id="70466-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="70466-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70466-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="70466-131">Formula</span></span>  <br/> |<span data-ttu-id="70466-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70466-132">xsd:string</span></span>  <br/> |<span data-ttu-id="70466-133">opcional</span><span class="sxs-lookup"><span data-stu-id="70466-133">optional</span></span>  <br/> |<span data-ttu-id="70466-134">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="70466-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="70466-135">Valores da cadeia de caracteres xsd:.</span><span class="sxs-lookup"><span data-stu-id="70466-135">Values of the xsd:string.</span></span>  <br/> |
   

