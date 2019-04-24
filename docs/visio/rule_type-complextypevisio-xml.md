---
title: Rule_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283419"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="f2523-102">Rule_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f2523-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f2523-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f2523-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2523-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f2523-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f2523-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f2523-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f2523-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f2523-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f2523-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f2523-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f2523-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f2523-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f2523-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f2523-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f2523-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f2523-110">Elements and attributes</span></span>

<span data-ttu-id="f2523-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f2523-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f2523-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f2523-112">Child elements</span></span>

|<span data-ttu-id="f2523-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2523-113">**Element**</span></span>|<span data-ttu-id="f2523-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f2523-114">**Type**</span></span>|<span data-ttu-id="f2523-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f2523-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f2523-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="f2523-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f2523-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="f2523-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f2523-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="f2523-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f2523-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="f2523-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f2523-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2523-120">Attributes</span></span>

|<span data-ttu-id="f2523-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f2523-121">**Attribute**</span></span>|<span data-ttu-id="f2523-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f2523-122">**Type**</span></span>|<span data-ttu-id="f2523-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f2523-123">**Required**</span></span>|<span data-ttu-id="f2523-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f2523-124">**Description**</span></span>|<span data-ttu-id="f2523-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f2523-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f2523-126">Categoria</span><span class="sxs-lookup"><span data-stu-id="f2523-126">Category</span></span>  <br/> |<span data-ttu-id="f2523-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f2523-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f2523-128">opcional</span><span class="sxs-lookup"><span data-stu-id="f2523-128">optional</span></span>  <br/> ||<span data-ttu-id="f2523-129">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f2523-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f2523-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2523-130">Description</span></span>  <br/> |<span data-ttu-id="f2523-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f2523-131">xsd:string</span></span>  <br/> |<span data-ttu-id="f2523-132">opcional</span><span class="sxs-lookup"><span data-stu-id="f2523-132">optional</span></span>  <br/> ||<span data-ttu-id="f2523-133">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f2523-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f2523-134">ID</span><span class="sxs-lookup"><span data-stu-id="f2523-134">ID</span></span>  <br/> |<span data-ttu-id="f2523-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f2523-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f2523-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f2523-136">required</span></span>  <br/> ||<span data-ttu-id="f2523-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f2523-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f2523-138">Ignorado</span><span class="sxs-lookup"><span data-stu-id="f2523-138">Ignored</span></span>  <br/> |<span data-ttu-id="f2523-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f2523-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f2523-140">opcional</span><span class="sxs-lookup"><span data-stu-id="f2523-140">optional</span></span>  <br/> ||<span data-ttu-id="f2523-141">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f2523-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f2523-142">NameU</span><span class="sxs-lookup"><span data-stu-id="f2523-142">NameU</span></span>  <br/> |<span data-ttu-id="f2523-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f2523-143">xsd:string</span></span>  <br/> |<span data-ttu-id="f2523-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f2523-144">required</span></span>  <br/> ||<span data-ttu-id="f2523-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f2523-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f2523-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="f2523-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="f2523-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="f2523-147">xsd:int</span></span>  <br/> |<span data-ttu-id="f2523-148">opcional</span><span class="sxs-lookup"><span data-stu-id="f2523-148">optional</span></span>  <br/> ||<span data-ttu-id="f2523-149">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="f2523-149">Values of the xsd:int type.</span></span>  <br/> |
   

