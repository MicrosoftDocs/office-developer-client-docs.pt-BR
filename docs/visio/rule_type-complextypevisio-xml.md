---
title: Rule_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541712"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="98b00-102">Rule_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="98b00-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="98b00-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="98b00-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98b00-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="98b00-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="98b00-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="98b00-105">**Schema file**</span></span> <br/> |<span data-ttu-id="98b00-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="98b00-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="98b00-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="98b00-107">**Extension base**</span></span> <br/> |<span data-ttu-id="98b00-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="98b00-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98b00-109">Definição</span><span class="sxs-lookup"><span data-stu-id="98b00-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="98b00-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="98b00-110">Elements and attributes</span></span>

<span data-ttu-id="98b00-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="98b00-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="98b00-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="98b00-112">Child elements</span></span>

|<span data-ttu-id="98b00-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="98b00-113">**Element**</span></span>|<span data-ttu-id="98b00-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="98b00-114">**Type**</span></span>|<span data-ttu-id="98b00-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98b00-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98b00-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="98b00-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="98b00-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="98b00-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="98b00-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="98b00-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="98b00-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="98b00-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="98b00-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="98b00-120">Attributes</span></span>

|<span data-ttu-id="98b00-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="98b00-121">**Attribute**</span></span>|<span data-ttu-id="98b00-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="98b00-122">**Type**</span></span>|<span data-ttu-id="98b00-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="98b00-123">**Required**</span></span>|<span data-ttu-id="98b00-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98b00-124">**Description**</span></span>|<span data-ttu-id="98b00-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="98b00-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98b00-126">Categoria</span><span class="sxs-lookup"><span data-stu-id="98b00-126">Category</span></span>  <br/> |<span data-ttu-id="98b00-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="98b00-127">xsd:string</span></span>  <br/> |<span data-ttu-id="98b00-128">opcional</span><span class="sxs-lookup"><span data-stu-id="98b00-128">optional</span></span>  <br/> ||<span data-ttu-id="98b00-129">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98b00-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="98b00-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="98b00-130">Description</span></span>  <br/> |<span data-ttu-id="98b00-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="98b00-131">xsd:string</span></span>  <br/> |<span data-ttu-id="98b00-132">opcional</span><span class="sxs-lookup"><span data-stu-id="98b00-132">optional</span></span>  <br/> ||<span data-ttu-id="98b00-133">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98b00-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="98b00-134">ID</span><span class="sxs-lookup"><span data-stu-id="98b00-134">ID</span></span>  <br/> |<span data-ttu-id="98b00-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="98b00-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="98b00-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="98b00-136">required</span></span>  <br/> ||<span data-ttu-id="98b00-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="98b00-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="98b00-138">Ignorado</span><span class="sxs-lookup"><span data-stu-id="98b00-138">Ignored</span></span>  <br/> |<span data-ttu-id="98b00-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="98b00-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="98b00-140">opcional</span><span class="sxs-lookup"><span data-stu-id="98b00-140">optional</span></span>  <br/> ||<span data-ttu-id="98b00-141">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="98b00-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="98b00-142">NameU</span><span class="sxs-lookup"><span data-stu-id="98b00-142">NameU</span></span>  <br/> |<span data-ttu-id="98b00-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="98b00-143">xsd:string</span></span>  <br/> |<span data-ttu-id="98b00-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="98b00-144">required</span></span>  <br/> ||<span data-ttu-id="98b00-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98b00-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="98b00-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="98b00-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="98b00-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="98b00-147">xsd:int</span></span>  <br/> |<span data-ttu-id="98b00-148">opcional</span><span class="sxs-lookup"><span data-stu-id="98b00-148">optional</span></span>  <br/> ||<span data-ttu-id="98b00-149">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="98b00-149">Values of the xsd:int type.</span></span>  <br/> |
   

