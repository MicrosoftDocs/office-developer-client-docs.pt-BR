---
title: RuleSet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772827"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="6182f-102">RuleSet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6182f-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6182f-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="6182f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6182f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6182f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6182f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6182f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6182f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6182f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6182f-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="6182f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6182f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6182f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6182f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6182f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6182f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6182f-110">Elements and attributes</span></span>

<span data-ttu-id="6182f-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6182f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6182f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6182f-112">Child elements</span></span>

|<span data-ttu-id="6182f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6182f-113">**Element**</span></span>|<span data-ttu-id="6182f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6182f-114">**Type**</span></span>|<span data-ttu-id="6182f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6182f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6182f-116">Rule</span><span class="sxs-lookup"><span data-stu-id="6182f-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6182f-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="6182f-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6182f-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="6182f-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6182f-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="6182f-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6182f-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="6182f-120">Attributes</span></span>

|<span data-ttu-id="6182f-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6182f-121">**Attribute**</span></span>|<span data-ttu-id="6182f-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6182f-122">**Type**</span></span>|<span data-ttu-id="6182f-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6182f-123">**Required**</span></span>|<span data-ttu-id="6182f-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6182f-124">**Description**</span></span>|<span data-ttu-id="6182f-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6182f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6182f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="6182f-126">Description</span></span>  <br/> |<span data-ttu-id="6182f-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6182f-127">xsd:string</span></span>  <br/> |<span data-ttu-id="6182f-128">opcional</span><span class="sxs-lookup"><span data-stu-id="6182f-128">optional</span></span>  <br/> ||<span data-ttu-id="6182f-129">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6182f-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6182f-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="6182f-130">Enabled</span></span>  <br/> |<span data-ttu-id="6182f-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6182f-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6182f-132">opcional</span><span class="sxs-lookup"><span data-stu-id="6182f-132">optional</span></span>  <br/> ||<span data-ttu-id="6182f-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6182f-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6182f-134">ID</span><span class="sxs-lookup"><span data-stu-id="6182f-134">ID</span></span>  <br/> |<span data-ttu-id="6182f-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6182f-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6182f-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6182f-136">required</span></span>  <br/> ||<span data-ttu-id="6182f-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6182f-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6182f-138">Nome</span><span class="sxs-lookup"><span data-stu-id="6182f-138">Name</span></span>  <br/> |<span data-ttu-id="6182f-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6182f-139">xsd:string</span></span>  <br/> |<span data-ttu-id="6182f-140">opcional</span><span class="sxs-lookup"><span data-stu-id="6182f-140">optional</span></span>  <br/> ||<span data-ttu-id="6182f-141">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6182f-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6182f-142">NameU</span><span class="sxs-lookup"><span data-stu-id="6182f-142">NameU</span></span>  <br/> |<span data-ttu-id="6182f-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6182f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6182f-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6182f-144">required</span></span>  <br/> ||<span data-ttu-id="6182f-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6182f-145">Values of the xsd:string type.</span></span>  <br/> |
   

