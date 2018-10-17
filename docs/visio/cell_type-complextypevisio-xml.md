---
title: Cell_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389460"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="bdd09-102">Cell_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bdd09-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bdd09-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="bdd09-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdd09-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bdd09-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bdd09-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bdd09-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bdd09-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bdd09-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bdd09-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="bdd09-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bdd09-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdd09-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bdd09-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bdd09-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bdd09-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bdd09-110">Elements and attributes</span></span>

<span data-ttu-id="bdd09-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bdd09-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bdd09-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bdd09-112">Child elements</span></span>

|<span data-ttu-id="bdd09-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bdd09-113">**Element**</span></span>|<span data-ttu-id="bdd09-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bdd09-114">**Type**</span></span>|<span data-ttu-id="bdd09-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bdd09-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bdd09-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="bdd09-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bdd09-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="bdd09-117">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bdd09-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdd09-118">Attributes</span></span>

|<span data-ttu-id="bdd09-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bdd09-119">**Attribute**</span></span>|<span data-ttu-id="bdd09-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bdd09-120">**Type**</span></span>|<span data-ttu-id="bdd09-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bdd09-121">**Required**</span></span>|<span data-ttu-id="bdd09-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bdd09-122">**Description**</span></span>|<span data-ttu-id="bdd09-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bdd09-123">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bdd09-124">E</span><span class="sxs-lookup"><span data-stu-id="bdd09-124">E</span></span>  <br/> |<span data-ttu-id="bdd09-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdd09-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bdd09-126">opcional</span><span class="sxs-lookup"><span data-stu-id="bdd09-126">optional</span></span>  <br/> ||<span data-ttu-id="bdd09-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdd09-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdd09-128">F</span><span class="sxs-lookup"><span data-stu-id="bdd09-128">F</span></span>  <br/> |<span data-ttu-id="bdd09-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdd09-129">xsd:string</span></span>  <br/> |<span data-ttu-id="bdd09-130">opcional</span><span class="sxs-lookup"><span data-stu-id="bdd09-130">optional</span></span>  <br/> ||<span data-ttu-id="bdd09-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdd09-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdd09-132">N</span><span class="sxs-lookup"><span data-stu-id="bdd09-132">N</span></span>  <br/> |<span data-ttu-id="bdd09-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdd09-133">xsd:string</span></span>  <br/> |<span data-ttu-id="bdd09-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdd09-134">required</span></span>  <br/> ||<span data-ttu-id="bdd09-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdd09-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdd09-136">S</span><span class="sxs-lookup"><span data-stu-id="bdd09-136">U</span></span>  <br/> |<span data-ttu-id="bdd09-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdd09-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bdd09-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bdd09-138">optional</span></span>  <br/> ||<span data-ttu-id="bdd09-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdd09-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdd09-140">S</span><span class="sxs-lookup"><span data-stu-id="bdd09-140">v</span></span>  <br/> |<span data-ttu-id="bdd09-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdd09-141">xsd:string</span></span>  <br/> |<span data-ttu-id="bdd09-142">opcional</span><span class="sxs-lookup"><span data-stu-id="bdd09-142">optional</span></span>  <br/> ||<span data-ttu-id="bdd09-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdd09-143">Values of the xsd:string type.</span></span>  <br/> |
   

