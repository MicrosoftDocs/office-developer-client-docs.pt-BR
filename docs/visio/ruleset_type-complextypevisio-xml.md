---
title: RuleSet_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 5d3d29ee7ae48c344afcdce3faf5e26d5f564501
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541621"
---
# <a name="ruleset_type-complextype-visio-xml"></a><span data-ttu-id="412cb-102">RuleSet_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="412cb-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="412cb-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="412cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="412cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="412cb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="412cb-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="412cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="412cb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="412cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="412cb-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="412cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="412cb-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="412cb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="412cb-109">Definição</span><span class="sxs-lookup"><span data-stu-id="412cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="412cb-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="412cb-110">Elements and attributes</span></span>

<span data-ttu-id="412cb-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="412cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="412cb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="412cb-112">Child elements</span></span>

|<span data-ttu-id="412cb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="412cb-113">**Element**</span></span>|<span data-ttu-id="412cb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="412cb-114">**Type**</span></span>|<span data-ttu-id="412cb-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="412cb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="412cb-116">Rule</span><span class="sxs-lookup"><span data-stu-id="412cb-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="412cb-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="412cb-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="412cb-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="412cb-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="412cb-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="412cb-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="412cb-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="412cb-120">Attributes</span></span>

|<span data-ttu-id="412cb-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="412cb-121">**Attribute**</span></span>|<span data-ttu-id="412cb-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="412cb-122">**Type**</span></span>|<span data-ttu-id="412cb-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="412cb-123">**Required**</span></span>|<span data-ttu-id="412cb-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="412cb-124">**Description**</span></span>|<span data-ttu-id="412cb-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="412cb-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="412cb-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="412cb-126">Description</span></span>  <br/> |<span data-ttu-id="412cb-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="412cb-127">xsd:string</span></span>  <br/> |<span data-ttu-id="412cb-128">opcional</span><span class="sxs-lookup"><span data-stu-id="412cb-128">optional</span></span>  <br/> ||<span data-ttu-id="412cb-129">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="412cb-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="412cb-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="412cb-130">Enabled</span></span>  <br/> |<span data-ttu-id="412cb-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="412cb-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="412cb-132">opcional</span><span class="sxs-lookup"><span data-stu-id="412cb-132">optional</span></span>  <br/> ||<span data-ttu-id="412cb-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="412cb-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="412cb-134">ID</span><span class="sxs-lookup"><span data-stu-id="412cb-134">ID</span></span>  <br/> |<span data-ttu-id="412cb-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="412cb-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="412cb-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="412cb-136">required</span></span>  <br/> ||<span data-ttu-id="412cb-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="412cb-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="412cb-138">Nome</span><span class="sxs-lookup"><span data-stu-id="412cb-138">Name</span></span>  <br/> |<span data-ttu-id="412cb-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="412cb-139">xsd:string</span></span>  <br/> |<span data-ttu-id="412cb-140">opcional</span><span class="sxs-lookup"><span data-stu-id="412cb-140">optional</span></span>  <br/> ||<span data-ttu-id="412cb-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="412cb-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="412cb-142">NameU</span><span class="sxs-lookup"><span data-stu-id="412cb-142">NameU</span></span>  <br/> |<span data-ttu-id="412cb-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="412cb-143">xsd:string</span></span>  <br/> |<span data-ttu-id="412cb-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="412cb-144">required</span></span>  <br/> ||<span data-ttu-id="412cb-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="412cb-145">Values of the xsd:string type.</span></span>  <br/> |
   

