---
title: Elemento de validação ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Armazena informações sobre a validação de diagrama do documento.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382354"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="b5dc5-103">Elemento de validação ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b5dc5-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="b5dc5-104">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5dc5-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="b5dc5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5dc5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5dc5-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="b5dc5-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5dc5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5dc5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5dc5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5dc5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5dc5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5dc5-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="b5dc5-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5dc5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="b5dc5-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5dc5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b5dc5-114">Elements and attributes</span></span>

<span data-ttu-id="b5dc5-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5dc5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b5dc5-116">Parent elements</span></span>

<span data-ttu-id="b5dc5-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5dc5-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b5dc5-118">Child elements</span></span>

|<span data-ttu-id="b5dc5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-119">**Element**</span></span>|<span data-ttu-id="b5dc5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-120">**Type**</span></span>|<span data-ttu-id="b5dc5-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5dc5-122">Problemas</span><span class="sxs-lookup"><span data-stu-id="b5dc5-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5dc5-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b5dc5-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5dc5-124">Contém todos os elementos de **problema** para o documento.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="b5dc5-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="b5dc5-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5dc5-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="b5dc5-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5dc5-127">Inclui um elemento **RuleSet** para cada regra de validação definida no documento.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="b5dc5-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="b5dc5-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5dc5-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="b5dc5-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5dc5-130">Encapsula as propriedades relacionadas a validação do documento.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b5dc5-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5dc5-131">Attributes</span></span>

<span data-ttu-id="b5dc5-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-132">None.</span></span>
  

