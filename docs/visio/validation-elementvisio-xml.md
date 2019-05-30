---
title: Elemento validation (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Armazena informações sobre a validação de diagrama do documento.
ms.openlocfilehash: b1b1bcbd70d57d7a7316e91d137cf8c3c3750722
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538547"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="cf275-103">Elemento validation (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="cf275-103">Validation element (Visio XML)</span></span>

<span data-ttu-id="cf275-104">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="cf275-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf275-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="cf275-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf275-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cf275-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cf275-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="cf275-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cf275-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf275-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cf275-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf275-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cf275-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cf275-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cf275-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="cf275-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cf275-112">Validation. xml</span><span class="sxs-lookup"><span data-stu-id="cf275-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf275-113">Definição</span><span class="sxs-lookup"><span data-stu-id="cf275-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf275-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cf275-114">Elements and attributes</span></span>

<span data-ttu-id="cf275-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cf275-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf275-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cf275-116">Parent elements</span></span>

<span data-ttu-id="cf275-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cf275-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf275-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cf275-118">Child elements</span></span>

|<span data-ttu-id="cf275-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf275-119">**Element**</span></span>|<span data-ttu-id="cf275-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf275-120">**Type**</span></span>|<span data-ttu-id="cf275-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cf275-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf275-122">Issues</span><span class="sxs-lookup"><span data-stu-id="cf275-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf275-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="cf275-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf275-124">Contém todos os elementos **Issue** do documento.</span><span class="sxs-lookup"><span data-stu-id="cf275-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="cf275-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="cf275-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf275-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="cf275-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf275-127">Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="cf275-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="cf275-128">Validationproperties</span><span class="sxs-lookup"><span data-stu-id="cf275-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf275-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="cf275-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf275-130">Encapsula as propriedades relacionadas à validação do documento.</span><span class="sxs-lookup"><span data-stu-id="cf275-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cf275-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf275-131">Attributes</span></span>

<span data-ttu-id="cf275-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cf275-132">None.</span></span>
  

