---
title: RuleSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307739"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="85760-102">RuleSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="85760-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85760-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="85760-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85760-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85760-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85760-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85760-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85760-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="85760-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85760-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="85760-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85760-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="85760-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85760-109">Definição</span><span class="sxs-lookup"><span data-stu-id="85760-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85760-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="85760-110">Elements and attributes</span></span>

<span data-ttu-id="85760-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="85760-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85760-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="85760-112">Child elements</span></span>

|<span data-ttu-id="85760-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85760-113">**Element**</span></span>|<span data-ttu-id="85760-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85760-114">**Type**</span></span>|<span data-ttu-id="85760-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85760-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85760-116">Rule</span><span class="sxs-lookup"><span data-stu-id="85760-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85760-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="85760-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85760-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="85760-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85760-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="85760-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85760-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="85760-120">Attributes</span></span>

|<span data-ttu-id="85760-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="85760-121">**Attribute**</span></span>|<span data-ttu-id="85760-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85760-122">**Type**</span></span>|<span data-ttu-id="85760-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="85760-123">**Required**</span></span>|<span data-ttu-id="85760-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85760-124">**Description**</span></span>|<span data-ttu-id="85760-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="85760-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85760-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="85760-126">Description</span></span>  <br/> |<span data-ttu-id="85760-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85760-127">xsd:string</span></span>  <br/> |<span data-ttu-id="85760-128">opcional</span><span class="sxs-lookup"><span data-stu-id="85760-128">optional</span></span>  <br/> ||<span data-ttu-id="85760-129">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85760-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85760-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="85760-130">Enabled</span></span>  <br/> |<span data-ttu-id="85760-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="85760-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85760-132">opcional</span><span class="sxs-lookup"><span data-stu-id="85760-132">optional</span></span>  <br/> ||<span data-ttu-id="85760-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="85760-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="85760-134">ID</span><span class="sxs-lookup"><span data-stu-id="85760-134">ID</span></span>  <br/> |<span data-ttu-id="85760-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85760-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85760-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="85760-136">required</span></span>  <br/> ||<span data-ttu-id="85760-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85760-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85760-138">Nome</span><span class="sxs-lookup"><span data-stu-id="85760-138">Name</span></span>  <br/> |<span data-ttu-id="85760-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85760-139">xsd:string</span></span>  <br/> |<span data-ttu-id="85760-140">opcional</span><span class="sxs-lookup"><span data-stu-id="85760-140">optional</span></span>  <br/> ||<span data-ttu-id="85760-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85760-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85760-142">NameU</span><span class="sxs-lookup"><span data-stu-id="85760-142">NameU</span></span>  <br/> |<span data-ttu-id="85760-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85760-143">xsd:string</span></span>  <br/> |<span data-ttu-id="85760-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="85760-144">required</span></span>  <br/> ||<span data-ttu-id="85760-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85760-145">Values of the xsd:string type.</span></span>  <br/> |
   

