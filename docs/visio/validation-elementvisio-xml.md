---
title: Elemento validation (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Armazena informações sobre a validação de diagrama do documento.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329077"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="e7320-103">Elemento validation (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e7320-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="e7320-104">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="e7320-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7320-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="e7320-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7320-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e7320-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e7320-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="e7320-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e7320-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e7320-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e7320-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e7320-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e7320-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e7320-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e7320-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="e7320-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e7320-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="e7320-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e7320-113">Definição</span><span class="sxs-lookup"><span data-stu-id="e7320-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e7320-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e7320-114">Elements and attributes</span></span>

<span data-ttu-id="e7320-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e7320-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e7320-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e7320-116">Parent elements</span></span>

<span data-ttu-id="e7320-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e7320-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7320-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e7320-118">Child elements</span></span>

|<span data-ttu-id="e7320-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7320-119">**Element**</span></span>|<span data-ttu-id="e7320-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e7320-120">**Type**</span></span>|<span data-ttu-id="e7320-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e7320-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e7320-122">Issues</span><span class="sxs-lookup"><span data-stu-id="e7320-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e7320-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="e7320-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e7320-124">Contém todos os elementos **Issue** do documento.</span><span class="sxs-lookup"><span data-stu-id="e7320-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="e7320-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="e7320-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e7320-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="e7320-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e7320-127">Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="e7320-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="e7320-128">Validationproperties</span><span class="sxs-lookup"><span data-stu-id="e7320-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e7320-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="e7320-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e7320-130">Encapsula as propriedades relacionadas à validação do documento.</span><span class="sxs-lookup"><span data-stu-id="e7320-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e7320-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7320-131">Attributes</span></span>

<span data-ttu-id="e7320-132">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e7320-132">None.</span></span>
  

