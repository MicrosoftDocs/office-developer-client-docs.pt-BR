---
title: EventItem_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 7fc23d9e2a9e4567693a4979b796804b16f148e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771828"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="56a77-102">EventItem_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="56a77-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="56a77-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="56a77-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56a77-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="56a77-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="56a77-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="56a77-105">**Schema file**</span></span> <br/> |<span data-ttu-id="56a77-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="56a77-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="56a77-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="56a77-107">**Extension base**</span></span> <br/> |<span data-ttu-id="56a77-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="56a77-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56a77-109">Definição</span><span class="sxs-lookup"><span data-stu-id="56a77-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="56a77-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="56a77-110">Elements and attributes</span></span>

<span data-ttu-id="56a77-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="56a77-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="56a77-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="56a77-112">Child elements</span></span>

<span data-ttu-id="56a77-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="56a77-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56a77-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="56a77-114">Attributes</span></span>

|<span data-ttu-id="56a77-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="56a77-115">**Attribute**</span></span>|<span data-ttu-id="56a77-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="56a77-116">**Type**</span></span>|<span data-ttu-id="56a77-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="56a77-117">**Required**</span></span>|<span data-ttu-id="56a77-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="56a77-118">**Description**</span></span>|<span data-ttu-id="56a77-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="56a77-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="56a77-120">Ação</span><span class="sxs-lookup"><span data-stu-id="56a77-120">Action</span></span>  <br/> |<span data-ttu-id="56a77-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="56a77-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="56a77-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="56a77-122">required</span></span>  <br/> ||<span data-ttu-id="56a77-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="56a77-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="56a77-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="56a77-124">Enabled</span></span>  <br/> |<span data-ttu-id="56a77-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="56a77-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="56a77-126">opcional</span><span class="sxs-lookup"><span data-stu-id="56a77-126">optional</span></span>  <br/> ||<span data-ttu-id="56a77-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="56a77-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="56a77-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="56a77-128">EventCode</span></span>  <br/> |<span data-ttu-id="56a77-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="56a77-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="56a77-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="56a77-130">required</span></span>  <br/> ||<span data-ttu-id="56a77-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="56a77-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="56a77-132">ID</span><span class="sxs-lookup"><span data-stu-id="56a77-132">ID</span></span>  <br/> |<span data-ttu-id="56a77-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="56a77-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="56a77-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="56a77-134">required</span></span>  <br/> ||<span data-ttu-id="56a77-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="56a77-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="56a77-136">Destino</span><span class="sxs-lookup"><span data-stu-id="56a77-136">Target</span></span>  <br/> |<span data-ttu-id="56a77-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="56a77-137">xsd:string</span></span>  <br/> |<span data-ttu-id="56a77-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="56a77-138">required</span></span>  <br/> ||<span data-ttu-id="56a77-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="56a77-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="56a77-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="56a77-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="56a77-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="56a77-141">xsd:string</span></span>  <br/> |<span data-ttu-id="56a77-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="56a77-142">required</span></span>  <br/> ||<span data-ttu-id="56a77-143">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="56a77-143">Values of the xsd:string type.</span></span>  <br/> |
   

