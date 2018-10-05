---
title: Rule_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393506"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="34ec0-102">Rule_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="34ec0-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="34ec0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="34ec0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34ec0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34ec0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="34ec0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="34ec0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="34ec0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="34ec0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="34ec0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="34ec0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="34ec0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="34ec0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34ec0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="34ec0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="34ec0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="34ec0-110">Elements and attributes</span></span>

<span data-ttu-id="34ec0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="34ec0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="34ec0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="34ec0-112">Child elements</span></span>

|<span data-ttu-id="34ec0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="34ec0-113">**Element**</span></span>|<span data-ttu-id="34ec0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34ec0-114">**Type**</span></span>|<span data-ttu-id="34ec0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34ec0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34ec0-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="34ec0-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34ec0-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="34ec0-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="34ec0-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="34ec0-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34ec0-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="34ec0-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="34ec0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="34ec0-120">Attributes</span></span>

|<span data-ttu-id="34ec0-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="34ec0-121">**Attribute**</span></span>|<span data-ttu-id="34ec0-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34ec0-122">**Type**</span></span>|<span data-ttu-id="34ec0-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="34ec0-123">**Required**</span></span>|<span data-ttu-id="34ec0-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34ec0-124">**Description**</span></span>|<span data-ttu-id="34ec0-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="34ec0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="34ec0-126">Category</span><span class="sxs-lookup"><span data-stu-id="34ec0-126">Category</span></span>  <br/> |<span data-ttu-id="34ec0-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34ec0-127">xsd:string</span></span>  <br/> |<span data-ttu-id="34ec0-128">opcional</span><span class="sxs-lookup"><span data-stu-id="34ec0-128">optional</span></span>  <br/> ||<span data-ttu-id="34ec0-129">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34ec0-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34ec0-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="34ec0-130">Description</span></span>  <br/> |<span data-ttu-id="34ec0-131">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34ec0-131">xsd:string</span></span>  <br/> |<span data-ttu-id="34ec0-132">opcional</span><span class="sxs-lookup"><span data-stu-id="34ec0-132">optional</span></span>  <br/> ||<span data-ttu-id="34ec0-133">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34ec0-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34ec0-134">ID</span><span class="sxs-lookup"><span data-stu-id="34ec0-134">ID</span></span>  <br/> |<span data-ttu-id="34ec0-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34ec0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34ec0-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="34ec0-136">required</span></span>  <br/> ||<span data-ttu-id="34ec0-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="34ec0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34ec0-138">Ignorado</span><span class="sxs-lookup"><span data-stu-id="34ec0-138">Ignored</span></span>  <br/> |<span data-ttu-id="34ec0-139">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="34ec0-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="34ec0-140">opcional</span><span class="sxs-lookup"><span data-stu-id="34ec0-140">optional</span></span>  <br/> ||<span data-ttu-id="34ec0-141">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="34ec0-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="34ec0-142">NameU</span><span class="sxs-lookup"><span data-stu-id="34ec0-142">NameU</span></span>  <br/> |<span data-ttu-id="34ec0-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34ec0-143">xsd:string</span></span>  <br/> |<span data-ttu-id="34ec0-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="34ec0-144">required</span></span>  <br/> ||<span data-ttu-id="34ec0-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34ec0-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34ec0-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="34ec0-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="34ec0-147">XSD:int</span><span class="sxs-lookup"><span data-stu-id="34ec0-147">xsd:int</span></span>  <br/> |<span data-ttu-id="34ec0-148">opcional</span><span class="sxs-lookup"><span data-stu-id="34ec0-148">optional</span></span>  <br/> ||<span data-ttu-id="34ec0-149">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="34ec0-149">Values of the xsd:int type.</span></span>  <br/> |
   

