---
title: FaceName_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542895"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="6d697-102">FaceName_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="6d697-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6d697-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="6d697-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d697-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d697-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d697-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d697-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d697-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6d697-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d697-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="6d697-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d697-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6d697-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d697-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6d697-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d697-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6d697-110">Elements and attributes</span></span>

<span data-ttu-id="6d697-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6d697-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d697-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6d697-112">Child elements</span></span>

<span data-ttu-id="6d697-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6d697-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d697-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d697-114">Attributes</span></span>

|<span data-ttu-id="6d697-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6d697-115">**Attribute**</span></span>|<span data-ttu-id="6d697-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6d697-116">**Type**</span></span>|<span data-ttu-id="6d697-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6d697-117">**Required**</span></span>|<span data-ttu-id="6d697-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d697-118">**Description**</span></span>|<span data-ttu-id="6d697-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6d697-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d697-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="6d697-120">CharSets</span></span>  <br/> |<span data-ttu-id="6d697-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d697-121">xsd:string</span></span>  <br/> |<span data-ttu-id="6d697-122">opcional</span><span class="sxs-lookup"><span data-stu-id="6d697-122">optional</span></span>  <br/> ||<span data-ttu-id="6d697-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6d697-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d697-124">Sinalizadores</span><span class="sxs-lookup"><span data-stu-id="6d697-124">Flags</span></span>  <br/> |<span data-ttu-id="6d697-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d697-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d697-126">opcional</span><span class="sxs-lookup"><span data-stu-id="6d697-126">optional</span></span>  <br/> ||<span data-ttu-id="6d697-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d697-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d697-128">NameU</span><span class="sxs-lookup"><span data-stu-id="6d697-128">NameU</span></span>  <br/> |<span data-ttu-id="6d697-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d697-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6d697-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6d697-130">required</span></span>  <br/> ||<span data-ttu-id="6d697-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6d697-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d697-132">Panos</span><span class="sxs-lookup"><span data-stu-id="6d697-132">Panos</span></span>  <br/> |<span data-ttu-id="6d697-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d697-133">xsd:string</span></span>  <br/> |<span data-ttu-id="6d697-134">opcional</span><span class="sxs-lookup"><span data-stu-id="6d697-134">optional</span></span>  <br/> ||<span data-ttu-id="6d697-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6d697-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d697-136">Panose</span><span class="sxs-lookup"><span data-stu-id="6d697-136">Panose</span></span>  <br/> |<span data-ttu-id="6d697-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d697-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6d697-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6d697-138">optional</span></span>  <br/> ||<span data-ttu-id="6d697-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6d697-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d697-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="6d697-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="6d697-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d697-141">xsd:string</span></span>  <br/> |<span data-ttu-id="6d697-142">opcional</span><span class="sxs-lookup"><span data-stu-id="6d697-142">optional</span></span>  <br/> ||<span data-ttu-id="6d697-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6d697-143">Values of the xsd:string type.</span></span>  <br/> |
   

