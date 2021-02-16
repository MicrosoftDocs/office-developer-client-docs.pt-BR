---
title: EventItem_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541789"
---
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="f76c2-102">EventItem_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f76c2-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f76c2-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f76c2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f76c2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f76c2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f76c2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f76c2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f76c2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f76c2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f76c2-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f76c2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f76c2-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f76c2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f76c2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f76c2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f76c2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f76c2-110">Elements and attributes</span></span>

<span data-ttu-id="f76c2-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f76c2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f76c2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f76c2-112">Child elements</span></span>

<span data-ttu-id="f76c2-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f76c2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f76c2-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f76c2-114">Attributes</span></span>

|<span data-ttu-id="f76c2-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f76c2-115">**Attribute**</span></span>|<span data-ttu-id="f76c2-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f76c2-116">**Type**</span></span>|<span data-ttu-id="f76c2-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f76c2-117">**Required**</span></span>|<span data-ttu-id="f76c2-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f76c2-118">**Description**</span></span>|<span data-ttu-id="f76c2-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f76c2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f76c2-120">Ação</span><span class="sxs-lookup"><span data-stu-id="f76c2-120">Action</span></span>  <br/> |<span data-ttu-id="f76c2-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f76c2-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f76c2-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f76c2-122">required</span></span>  <br/> ||<span data-ttu-id="f76c2-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f76c2-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f76c2-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="f76c2-124">Enabled</span></span>  <br/> |<span data-ttu-id="f76c2-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f76c2-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f76c2-126">opcional</span><span class="sxs-lookup"><span data-stu-id="f76c2-126">optional</span></span>  <br/> ||<span data-ttu-id="f76c2-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f76c2-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f76c2-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="f76c2-128">EventCode</span></span>  <br/> |<span data-ttu-id="f76c2-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f76c2-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f76c2-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f76c2-130">required</span></span>  <br/> ||<span data-ttu-id="f76c2-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f76c2-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f76c2-132">ID</span><span class="sxs-lookup"><span data-stu-id="f76c2-132">ID</span></span>  <br/> |<span data-ttu-id="f76c2-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f76c2-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f76c2-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f76c2-134">required</span></span>  <br/> ||<span data-ttu-id="f76c2-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f76c2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f76c2-136">Destino</span><span class="sxs-lookup"><span data-stu-id="f76c2-136">Target</span></span>  <br/> |<span data-ttu-id="f76c2-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f76c2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f76c2-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f76c2-138">required</span></span>  <br/> ||<span data-ttu-id="f76c2-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f76c2-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f76c2-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="f76c2-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="f76c2-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f76c2-141">xsd:string</span></span>  <br/> |<span data-ttu-id="f76c2-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f76c2-142">required</span></span>  <br/> ||<span data-ttu-id="f76c2-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f76c2-143">Values of the xsd:string type.</span></span>  <br/> |
   

