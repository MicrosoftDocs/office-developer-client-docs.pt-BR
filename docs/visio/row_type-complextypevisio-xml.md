---
title: Row_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: ebd3b666590e6144d2a3cb6e0059b64eb6e8dab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331644"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="5552b-102">Row_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5552b-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5552b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="5552b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5552b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5552b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5552b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5552b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5552b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5552b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5552b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="5552b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5552b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5552b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5552b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5552b-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5552b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5552b-110">Elements and attributes</span></span>

<span data-ttu-id="5552b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5552b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5552b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5552b-112">Child elements</span></span>

|<span data-ttu-id="5552b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5552b-113">**Element**</span></span>|<span data-ttu-id="5552b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5552b-114">**Type**</span></span>|<span data-ttu-id="5552b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5552b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5552b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5552b-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="5552b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5552b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5552b-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="5552b-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="5552b-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="5552b-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5552b-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="5552b-120">Attributes</span></span>

|<span data-ttu-id="5552b-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5552b-121">**Attribute**</span></span>|<span data-ttu-id="5552b-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5552b-122">**Type**</span></span>|<span data-ttu-id="5552b-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5552b-123">**Required**</span></span>|<span data-ttu-id="5552b-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5552b-124">**Description**</span></span>|<span data-ttu-id="5552b-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5552b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5552b-126">Del</span><span class="sxs-lookup"><span data-stu-id="5552b-126">Del</span></span>  <br/> |<span data-ttu-id="5552b-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5552b-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5552b-128">opcional</span><span class="sxs-lookup"><span data-stu-id="5552b-128">optional</span></span>  <br/> ||<span data-ttu-id="5552b-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5552b-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5552b-130">IX</span><span class="sxs-lookup"><span data-stu-id="5552b-130">IX</span></span>  <br/> |<span data-ttu-id="5552b-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5552b-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5552b-132">opcional</span><span class="sxs-lookup"><span data-stu-id="5552b-132">optional</span></span>  <br/> ||<span data-ttu-id="5552b-133">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5552b-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5552b-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="5552b-134">LocalName</span></span>  <br/> |<span data-ttu-id="5552b-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5552b-135">xsd:string</span></span>  <br/> |<span data-ttu-id="5552b-136">opcional</span><span class="sxs-lookup"><span data-stu-id="5552b-136">optional</span></span>  <br/> ||<span data-ttu-id="5552b-137">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5552b-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5552b-138">N</span><span class="sxs-lookup"><span data-stu-id="5552b-138">N</span></span>  <br/> |<span data-ttu-id="5552b-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5552b-139">xsd:string</span></span>  <br/> |<span data-ttu-id="5552b-140">opcional</span><span class="sxs-lookup"><span data-stu-id="5552b-140">optional</span></span>  <br/> ||<span data-ttu-id="5552b-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5552b-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5552b-142">T</span><span class="sxs-lookup"><span data-stu-id="5552b-142">T</span></span>  <br/> |<span data-ttu-id="5552b-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5552b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5552b-144">opcional</span><span class="sxs-lookup"><span data-stu-id="5552b-144">optional</span></span>  <br/> ||<span data-ttu-id="5552b-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5552b-145">Values of the xsd:string type.</span></span>  <br/> |
   

