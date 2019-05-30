---
title: Connect_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538736"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="672a8-102">Connect_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="672a8-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="672a8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="672a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="672a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="672a8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="672a8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="672a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="672a8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="672a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="672a8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="672a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="672a8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="672a8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="672a8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="672a8-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="672a8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="672a8-110">Elements and attributes</span></span>

<span data-ttu-id="672a8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="672a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="672a8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="672a8-112">Child elements</span></span>

<span data-ttu-id="672a8-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="672a8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="672a8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="672a8-114">Attributes</span></span>

|<span data-ttu-id="672a8-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="672a8-115">**Attribute**</span></span>|<span data-ttu-id="672a8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="672a8-116">**Type**</span></span>|<span data-ttu-id="672a8-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="672a8-117">**Required**</span></span>|<span data-ttu-id="672a8-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="672a8-118">**Description**</span></span>|<span data-ttu-id="672a8-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="672a8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="672a8-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="672a8-120">FromCell</span></span>  <br/> |<span data-ttu-id="672a8-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="672a8-121">xsd:string</span></span>  <br/> |<span data-ttu-id="672a8-122">opcional</span><span class="sxs-lookup"><span data-stu-id="672a8-122">optional</span></span>  <br/> ||<span data-ttu-id="672a8-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="672a8-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="672a8-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="672a8-124">FromPart</span></span>  <br/> |<span data-ttu-id="672a8-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="672a8-125">xsd:int</span></span>  <br/> |<span data-ttu-id="672a8-126">opcional</span><span class="sxs-lookup"><span data-stu-id="672a8-126">optional</span></span>  <br/> ||<span data-ttu-id="672a8-127">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="672a8-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="672a8-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="672a8-128">FromSheet</span></span>  <br/> |<span data-ttu-id="672a8-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="672a8-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="672a8-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="672a8-130">required</span></span>  <br/> ||<span data-ttu-id="672a8-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="672a8-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="672a8-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="672a8-132">ToCell</span></span>  <br/> |<span data-ttu-id="672a8-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="672a8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="672a8-134">opcional</span><span class="sxs-lookup"><span data-stu-id="672a8-134">optional</span></span>  <br/> ||<span data-ttu-id="672a8-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="672a8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="672a8-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="672a8-136">ToPart</span></span>  <br/> |<span data-ttu-id="672a8-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="672a8-137">xsd:int</span></span>  <br/> |<span data-ttu-id="672a8-138">opcional</span><span class="sxs-lookup"><span data-stu-id="672a8-138">optional</span></span>  <br/> ||<span data-ttu-id="672a8-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="672a8-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="672a8-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="672a8-140">ToSheet</span></span>  <br/> |<span data-ttu-id="672a8-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="672a8-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="672a8-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="672a8-142">required</span></span>  <br/> ||<span data-ttu-id="672a8-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="672a8-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

