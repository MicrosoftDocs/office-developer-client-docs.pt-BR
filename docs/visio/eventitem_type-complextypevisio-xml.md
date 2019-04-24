---
title: EventItem_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337202"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="cbec6-102">EventItem_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cbec6-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cbec6-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="cbec6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbec6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cbec6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cbec6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cbec6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cbec6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cbec6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cbec6-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="cbec6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cbec6-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cbec6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cbec6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="cbec6-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cbec6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cbec6-110">Elements and attributes</span></span>

<span data-ttu-id="cbec6-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cbec6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cbec6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cbec6-112">Child elements</span></span>

<span data-ttu-id="cbec6-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cbec6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbec6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cbec6-114">Attributes</span></span>

|<span data-ttu-id="cbec6-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cbec6-115">**Attribute**</span></span>|<span data-ttu-id="cbec6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cbec6-116">**Type**</span></span>|<span data-ttu-id="cbec6-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cbec6-117">**Required**</span></span>|<span data-ttu-id="cbec6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbec6-118">**Description**</span></span>|<span data-ttu-id="cbec6-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cbec6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cbec6-120">Ação</span><span class="sxs-lookup"><span data-stu-id="cbec6-120">Action</span></span>  <br/> |<span data-ttu-id="cbec6-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cbec6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cbec6-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbec6-122">required</span></span>  <br/> ||<span data-ttu-id="cbec6-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cbec6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cbec6-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="cbec6-124">Enabled</span></span>  <br/> |<span data-ttu-id="cbec6-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cbec6-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cbec6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cbec6-126">optional</span></span>  <br/> ||<span data-ttu-id="cbec6-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cbec6-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cbec6-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="cbec6-128">EventCode</span></span>  <br/> |<span data-ttu-id="cbec6-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cbec6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cbec6-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbec6-130">required</span></span>  <br/> ||<span data-ttu-id="cbec6-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cbec6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cbec6-132">ID</span><span class="sxs-lookup"><span data-stu-id="cbec6-132">ID</span></span>  <br/> |<span data-ttu-id="cbec6-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cbec6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cbec6-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbec6-134">required</span></span>  <br/> ||<span data-ttu-id="cbec6-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cbec6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cbec6-136">Destino</span><span class="sxs-lookup"><span data-stu-id="cbec6-136">Target</span></span>  <br/> |<span data-ttu-id="cbec6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cbec6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="cbec6-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbec6-138">required</span></span>  <br/> ||<span data-ttu-id="cbec6-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cbec6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cbec6-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="cbec6-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="cbec6-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cbec6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="cbec6-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbec6-142">required</span></span>  <br/> ||<span data-ttu-id="cbec6-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cbec6-143">Values of the xsd:string type.</span></span>  <br/> |
   

