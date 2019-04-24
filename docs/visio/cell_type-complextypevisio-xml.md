---
title: Cell_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327115"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="38d2d-102">Cell_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="38d2d-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="38d2d-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="38d2d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38d2d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38d2d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="38d2d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="38d2d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="38d2d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="38d2d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="38d2d-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="38d2d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="38d2d-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="38d2d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38d2d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="38d2d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="38d2d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="38d2d-110">Elements and attributes</span></span>

<span data-ttu-id="38d2d-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="38d2d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="38d2d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="38d2d-112">Child elements</span></span>

|<span data-ttu-id="38d2d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="38d2d-113">**Element**</span></span>|<span data-ttu-id="38d2d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38d2d-114">**Type**</span></span>|<span data-ttu-id="38d2d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38d2d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38d2d-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="38d2d-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="38d2d-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="38d2d-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="38d2d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="38d2d-118">Attributes</span></span>

|<span data-ttu-id="38d2d-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="38d2d-119">**Attribute**</span></span>|<span data-ttu-id="38d2d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38d2d-120">**Type**</span></span>|<span data-ttu-id="38d2d-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="38d2d-121">**Required**</span></span>|<span data-ttu-id="38d2d-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38d2d-122">**Description**</span></span>|<span data-ttu-id="38d2d-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="38d2d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38d2d-124">E</span><span class="sxs-lookup"><span data-stu-id="38d2d-124">E</span></span>  <br/> |<span data-ttu-id="38d2d-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38d2d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="38d2d-126">opcional</span><span class="sxs-lookup"><span data-stu-id="38d2d-126">optional</span></span>  <br/> ||<span data-ttu-id="38d2d-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38d2d-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38d2d-128">F</span><span class="sxs-lookup"><span data-stu-id="38d2d-128">F</span></span>  <br/> |<span data-ttu-id="38d2d-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38d2d-129">xsd:string</span></span>  <br/> |<span data-ttu-id="38d2d-130">opcional</span><span class="sxs-lookup"><span data-stu-id="38d2d-130">optional</span></span>  <br/> ||<span data-ttu-id="38d2d-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38d2d-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38d2d-132">N</span><span class="sxs-lookup"><span data-stu-id="38d2d-132">N</span></span>  <br/> |<span data-ttu-id="38d2d-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38d2d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="38d2d-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="38d2d-134">required</span></span>  <br/> ||<span data-ttu-id="38d2d-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38d2d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38d2d-136">S</span><span class="sxs-lookup"><span data-stu-id="38d2d-136">U</span></span>  <br/> |<span data-ttu-id="38d2d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38d2d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="38d2d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="38d2d-138">optional</span></span>  <br/> ||<span data-ttu-id="38d2d-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38d2d-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38d2d-140">S</span><span class="sxs-lookup"><span data-stu-id="38d2d-140">V</span></span>  <br/> |<span data-ttu-id="38d2d-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38d2d-141">xsd:string</span></span>  <br/> |<span data-ttu-id="38d2d-142">opcional</span><span class="sxs-lookup"><span data-stu-id="38d2d-142">optional</span></span>  <br/> ||<span data-ttu-id="38d2d-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38d2d-143">Values of the xsd:string type.</span></span>  <br/> |
   

