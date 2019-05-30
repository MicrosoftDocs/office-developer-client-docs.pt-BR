---
title: Cell_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542300"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="b935f-102">Cell_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="b935f-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b935f-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="b935f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b935f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b935f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b935f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b935f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b935f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b935f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b935f-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="b935f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b935f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b935f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b935f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b935f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b935f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b935f-110">Elements and attributes</span></span>

<span data-ttu-id="b935f-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b935f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b935f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b935f-112">Child elements</span></span>

|<span data-ttu-id="b935f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b935f-113">**Element**</span></span>|<span data-ttu-id="b935f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b935f-114">**Type**</span></span>|<span data-ttu-id="b935f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b935f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b935f-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="b935f-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b935f-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b935f-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b935f-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b935f-118">Attributes</span></span>

|<span data-ttu-id="b935f-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b935f-119">**Attribute**</span></span>|<span data-ttu-id="b935f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b935f-120">**Type**</span></span>|<span data-ttu-id="b935f-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b935f-121">**Required**</span></span>|<span data-ttu-id="b935f-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b935f-122">**Description**</span></span>|<span data-ttu-id="b935f-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b935f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b935f-124">E</span><span class="sxs-lookup"><span data-stu-id="b935f-124">E</span></span>  <br/> |<span data-ttu-id="b935f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b935f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="b935f-126">opcional</span><span class="sxs-lookup"><span data-stu-id="b935f-126">optional</span></span>  <br/> ||<span data-ttu-id="b935f-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b935f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b935f-128">F</span><span class="sxs-lookup"><span data-stu-id="b935f-128">F</span></span>  <br/> |<span data-ttu-id="b935f-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b935f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="b935f-130">opcional</span><span class="sxs-lookup"><span data-stu-id="b935f-130">optional</span></span>  <br/> ||<span data-ttu-id="b935f-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b935f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b935f-132">N</span><span class="sxs-lookup"><span data-stu-id="b935f-132">N</span></span>  <br/> |<span data-ttu-id="b935f-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b935f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="b935f-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b935f-134">required</span></span>  <br/> ||<span data-ttu-id="b935f-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b935f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b935f-136">S</span><span class="sxs-lookup"><span data-stu-id="b935f-136">U</span></span>  <br/> |<span data-ttu-id="b935f-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b935f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="b935f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b935f-138">optional</span></span>  <br/> ||<span data-ttu-id="b935f-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b935f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b935f-140">S</span><span class="sxs-lookup"><span data-stu-id="b935f-140">V</span></span>  <br/> |<span data-ttu-id="b935f-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b935f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="b935f-142">opcional</span><span class="sxs-lookup"><span data-stu-id="b935f-142">optional</span></span>  <br/> ||<span data-ttu-id="b935f-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b935f-143">Values of the xsd:string type.</span></span>  <br/> |
   

