---
title: Elemento RuleFilter (Rule_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772798"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="61bbb-103">Elemento RuleFilter (Rule_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="61bbb-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="61bbb-104">Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="61bbb-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61bbb-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="61bbb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61bbb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="61bbb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61bbb-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="61bbb-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61bbb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61bbb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61bbb-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="61bbb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61bbb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61bbb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61bbb-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="61bbb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61bbb-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="61bbb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61bbb-113">Definição</span><span class="sxs-lookup"><span data-stu-id="61bbb-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61bbb-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="61bbb-114">Elements and attributes</span></span>

<span data-ttu-id="61bbb-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="61bbb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61bbb-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="61bbb-116">Parent elements</span></span>

|<span data-ttu-id="61bbb-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="61bbb-117">**Element**</span></span>|<span data-ttu-id="61bbb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61bbb-118">**Type**</span></span>|<span data-ttu-id="61bbb-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="61bbb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61bbb-120">Rule</span><span class="sxs-lookup"><span data-stu-id="61bbb-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61bbb-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="61bbb-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61bbb-122">Representa uma regra de validação única em um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="61bbb-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61bbb-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="61bbb-123">Child elements</span></span>

<span data-ttu-id="61bbb-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="61bbb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61bbb-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="61bbb-125">Attributes</span></span>

|<span data-ttu-id="61bbb-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="61bbb-126">**Attribute**</span></span>|<span data-ttu-id="61bbb-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61bbb-127">**Type**</span></span>|<span data-ttu-id="61bbb-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="61bbb-128">**Required**</span></span>|<span data-ttu-id="61bbb-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="61bbb-129">**Description**</span></span>|<span data-ttu-id="61bbb-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="61bbb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61bbb-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="61bbb-131">Formula</span></span>  <br/> |<span data-ttu-id="61bbb-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="61bbb-132">xsd:string</span></span>  <br/> |<span data-ttu-id="61bbb-133">opcional</span><span class="sxs-lookup"><span data-stu-id="61bbb-133">optional</span></span>  <br/> |<span data-ttu-id="61bbb-134">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="61bbb-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="61bbb-135">Valores da xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61bbb-135">Values of the xsd:string.</span></span>  <br/> |
   

