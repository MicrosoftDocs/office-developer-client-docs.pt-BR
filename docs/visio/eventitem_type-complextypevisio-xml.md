---
title: EventItem_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395725"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="bdc13-102">EventItem_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bdc13-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bdc13-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="bdc13-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdc13-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bdc13-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bdc13-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bdc13-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bdc13-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bdc13-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bdc13-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="bdc13-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bdc13-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdc13-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bdc13-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bdc13-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bdc13-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bdc13-110">Elements and attributes</span></span>

<span data-ttu-id="bdc13-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bdc13-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bdc13-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bdc13-112">Child elements</span></span>

<span data-ttu-id="bdc13-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bdc13-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdc13-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdc13-114">Attributes</span></span>

|<span data-ttu-id="bdc13-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bdc13-115">**Attribute**</span></span>|<span data-ttu-id="bdc13-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bdc13-116">**Type**</span></span>|<span data-ttu-id="bdc13-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bdc13-117">**Required**</span></span>|<span data-ttu-id="bdc13-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bdc13-118">**Description**</span></span>|<span data-ttu-id="bdc13-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bdc13-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bdc13-120">Ação</span><span class="sxs-lookup"><span data-stu-id="bdc13-120">Action</span></span>  <br/> |<span data-ttu-id="bdc13-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdc13-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdc13-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdc13-122">required</span></span>  <br/> ||<span data-ttu-id="bdc13-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdc13-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdc13-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="bdc13-124">Enabled</span></span>  <br/> |<span data-ttu-id="bdc13-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="bdc13-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bdc13-126">opcional</span><span class="sxs-lookup"><span data-stu-id="bdc13-126">optional</span></span>  <br/> ||<span data-ttu-id="bdc13-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bdc13-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bdc13-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="bdc13-128">EventCode</span></span>  <br/> |<span data-ttu-id="bdc13-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdc13-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdc13-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdc13-130">required</span></span>  <br/> ||<span data-ttu-id="bdc13-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdc13-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdc13-132">ID</span><span class="sxs-lookup"><span data-stu-id="bdc13-132">ID</span></span>  <br/> |<span data-ttu-id="bdc13-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bdc13-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bdc13-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdc13-134">required</span></span>  <br/> ||<span data-ttu-id="bdc13-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bdc13-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bdc13-136">Destino</span><span class="sxs-lookup"><span data-stu-id="bdc13-136">Target</span></span>  <br/> |<span data-ttu-id="bdc13-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdc13-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bdc13-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdc13-138">required</span></span>  <br/> ||<span data-ttu-id="bdc13-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdc13-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdc13-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="bdc13-140">TargetArgs Property</span></span>  <br/> |<span data-ttu-id="bdc13-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bdc13-141">xsd:string</span></span>  <br/> |<span data-ttu-id="bdc13-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdc13-142">required</span></span>  <br/> ||<span data-ttu-id="bdc13-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bdc13-143">Values of the xsd:string type.</span></span>  <br/> |
   

