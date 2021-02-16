---
title: Elemento RuleSetFlags (RuleSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: Especifica as propriedades do conjunto de regras.
ms.openlocfilehash: 03b94abb2d9bbe1f611671a4ac37053747a486fb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541593"
---
# <a name="rulesetflags-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="47716-103">Elemento RuleSetFlags (RuleSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="47716-103">RuleSetFlags element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="47716-104">Especifica as propriedades do conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="47716-104">Specifies rule-set properties.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47716-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="47716-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47716-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="47716-106">**Element type**</span></span> <br/> |[<span data-ttu-id="47716-107">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="47716-107">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="47716-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47716-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="47716-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="47716-109">**Schema file**</span></span> <br/> |<span data-ttu-id="47716-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="47716-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="47716-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="47716-111">**Document parts**</span></span> <br/> |<span data-ttu-id="47716-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="47716-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47716-113">Definição</span><span class="sxs-lookup"><span data-stu-id="47716-113">Definition</span></span>

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47716-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="47716-114">Elements and attributes</span></span>

<span data-ttu-id="47716-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="47716-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="47716-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="47716-116">Parent elements</span></span>

|<span data-ttu-id="47716-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="47716-117">**Element**</span></span>|<span data-ttu-id="47716-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="47716-118">**Type**</span></span>|<span data-ttu-id="47716-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47716-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47716-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="47716-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="47716-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="47716-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47716-122">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="47716-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="47716-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="47716-123">Child elements</span></span>

<span data-ttu-id="47716-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="47716-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47716-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="47716-125">Attributes</span></span>

|<span data-ttu-id="47716-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="47716-126">**Attribute**</span></span>|<span data-ttu-id="47716-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="47716-127">**Type**</span></span>|<span data-ttu-id="47716-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="47716-128">**Required**</span></span>|<span data-ttu-id="47716-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47716-129">**Description**</span></span>|<span data-ttu-id="47716-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="47716-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47716-131">Hidden</span><span class="sxs-lookup"><span data-stu-id="47716-131">Hidden</span></span>  <br/> |<span data-ttu-id="47716-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="47716-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="47716-133">opcional</span><span class="sxs-lookup"><span data-stu-id="47716-133">optional</span></span>  <br/> |<span data-ttu-id="47716-134">Especifica se o conjunto de regras aparece na lista Regras a Verificar.</span><span class="sxs-lookup"><span data-stu-id="47716-134">Specifies whether the rule set appears in the Rules to Check list.</span></span>  <br/> |<span data-ttu-id="47716-135">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="47716-135">Values of the xsd:boolean type.</span></span>  <br/> |
   

