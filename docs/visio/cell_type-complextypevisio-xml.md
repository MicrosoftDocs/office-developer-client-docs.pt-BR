---
title: Cell_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771472"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="0df01-102">Cell_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0df01-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0df01-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="0df01-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0df01-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0df01-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0df01-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0df01-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0df01-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0df01-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0df01-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="0df01-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0df01-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0df01-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0df01-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0df01-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0df01-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0df01-110">Elements and attributes</span></span>

<span data-ttu-id="0df01-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0df01-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0df01-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0df01-112">Child elements</span></span>

|<span data-ttu-id="0df01-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0df01-113">**Element**</span></span>|<span data-ttu-id="0df01-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0df01-114">**Type**</span></span>|<span data-ttu-id="0df01-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0df01-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0df01-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="0df01-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0df01-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0df01-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0df01-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0df01-118">Attributes</span></span>

|<span data-ttu-id="0df01-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0df01-119">**Attribute**</span></span>|<span data-ttu-id="0df01-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0df01-120">**Type**</span></span>|<span data-ttu-id="0df01-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="0df01-121">**Required**</span></span>|<span data-ttu-id="0df01-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0df01-122">**Description**</span></span>|<span data-ttu-id="0df01-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="0df01-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0df01-124">E</span><span class="sxs-lookup"><span data-stu-id="0df01-124">E</span></span>  <br/> |<span data-ttu-id="0df01-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0df01-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0df01-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0df01-126">optional</span></span>  <br/> ||<span data-ttu-id="0df01-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0df01-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0df01-128">S</span><span class="sxs-lookup"><span data-stu-id="0df01-128">F</span></span>  <br/> |<span data-ttu-id="0df01-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0df01-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0df01-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0df01-130">optional</span></span>  <br/> ||<span data-ttu-id="0df01-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0df01-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0df01-132">N</span><span class="sxs-lookup"><span data-stu-id="0df01-132">N</span></span>  <br/> |<span data-ttu-id="0df01-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0df01-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0df01-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="0df01-134">required</span></span>  <br/> ||<span data-ttu-id="0df01-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0df01-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0df01-136">U</span><span class="sxs-lookup"><span data-stu-id="0df01-136">U</span></span>  <br/> |<span data-ttu-id="0df01-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0df01-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0df01-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0df01-138">optional</span></span>  <br/> ||<span data-ttu-id="0df01-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0df01-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0df01-140">V</span><span class="sxs-lookup"><span data-stu-id="0df01-140">V</span></span>  <br/> |<span data-ttu-id="0df01-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0df01-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0df01-142">opcional</span><span class="sxs-lookup"><span data-stu-id="0df01-142">optional</span></span>  <br/> ||<span data-ttu-id="0df01-143">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0df01-143">Values of the xsd:string type.</span></span>  <br/> |
   

