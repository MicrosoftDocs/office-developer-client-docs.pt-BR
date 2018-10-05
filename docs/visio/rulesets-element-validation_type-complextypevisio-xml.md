---
title: Elemento RuleSets (Validation_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Inclui um elemento RuleSet para cada regra de validação definida no documento.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399638"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="91336-103">Elemento RuleSets (Validation_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="91336-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="91336-104">Inclui um elemento **RuleSet** para cada regra de validação definida no documento.</span><span class="sxs-lookup"><span data-stu-id="91336-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="91336-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="91336-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91336-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="91336-106">**Element type**</span></span> <br/> |[<span data-ttu-id="91336-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="91336-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="91336-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91336-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="91336-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="91336-109">**Schema file**</span></span> <br/> |<span data-ttu-id="91336-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="91336-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="91336-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="91336-111">**Document parts**</span></span> <br/> |<span data-ttu-id="91336-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="91336-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91336-113">Definição</span><span class="sxs-lookup"><span data-stu-id="91336-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="91336-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="91336-114">Elements and attributes</span></span>

<span data-ttu-id="91336-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="91336-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="91336-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="91336-116">Parent elements</span></span>

|<span data-ttu-id="91336-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="91336-117">**Element**</span></span>|<span data-ttu-id="91336-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="91336-118">**Type**</span></span>|<span data-ttu-id="91336-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="91336-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91336-120">Validação</span><span class="sxs-lookup"><span data-stu-id="91336-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="91336-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="91336-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="91336-122">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="91336-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="91336-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="91336-123">Child elements</span></span>

|<span data-ttu-id="91336-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="91336-124">**Element**</span></span>|<span data-ttu-id="91336-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="91336-125">**Type**</span></span>|<span data-ttu-id="91336-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="91336-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91336-127">Conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="91336-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91336-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="91336-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="91336-129">Representa um conjunto de regras de validação de diagrama.</span><span class="sxs-lookup"><span data-stu-id="91336-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="91336-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="91336-130">Attributes</span></span>

<span data-ttu-id="91336-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="91336-131">None.</span></span>
  

