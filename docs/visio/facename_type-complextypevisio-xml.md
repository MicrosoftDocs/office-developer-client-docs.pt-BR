---
title: FaceName_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322551"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="4ec38-102">FaceName_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4ec38-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4ec38-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4ec38-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ec38-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ec38-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ec38-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4ec38-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ec38-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ec38-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ec38-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4ec38-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ec38-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4ec38-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ec38-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4ec38-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4ec38-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4ec38-110">Elements and attributes</span></span>

<span data-ttu-id="4ec38-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4ec38-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ec38-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4ec38-112">Child elements</span></span>

<span data-ttu-id="4ec38-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4ec38-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ec38-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ec38-114">Attributes</span></span>

|<span data-ttu-id="4ec38-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4ec38-115">**Attribute**</span></span>|<span data-ttu-id="4ec38-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4ec38-116">**Type**</span></span>|<span data-ttu-id="4ec38-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4ec38-117">**Required**</span></span>|<span data-ttu-id="4ec38-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ec38-118">**Description**</span></span>|<span data-ttu-id="4ec38-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4ec38-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ec38-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="4ec38-120">CharSets</span></span>  <br/> |<span data-ttu-id="4ec38-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4ec38-121">xsd:string</span></span>  <br/> |<span data-ttu-id="4ec38-122">opcional</span><span class="sxs-lookup"><span data-stu-id="4ec38-122">optional</span></span>  <br/> ||<span data-ttu-id="4ec38-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4ec38-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ec38-124">Sinalizadores</span><span class="sxs-lookup"><span data-stu-id="4ec38-124">Flags</span></span>  <br/> |<span data-ttu-id="4ec38-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4ec38-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4ec38-126">opcional</span><span class="sxs-lookup"><span data-stu-id="4ec38-126">optional</span></span>  <br/> ||<span data-ttu-id="4ec38-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4ec38-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4ec38-128">NameU</span><span class="sxs-lookup"><span data-stu-id="4ec38-128">NameU</span></span>  <br/> |<span data-ttu-id="4ec38-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4ec38-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4ec38-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ec38-130">required</span></span>  <br/> ||<span data-ttu-id="4ec38-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4ec38-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ec38-132">Panos</span><span class="sxs-lookup"><span data-stu-id="4ec38-132">Panos</span></span>  <br/> |<span data-ttu-id="4ec38-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4ec38-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4ec38-134">opcional</span><span class="sxs-lookup"><span data-stu-id="4ec38-134">optional</span></span>  <br/> ||<span data-ttu-id="4ec38-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4ec38-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ec38-136">Panose</span><span class="sxs-lookup"><span data-stu-id="4ec38-136">Panose</span></span>  <br/> |<span data-ttu-id="4ec38-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4ec38-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4ec38-138">opcional</span><span class="sxs-lookup"><span data-stu-id="4ec38-138">optional</span></span>  <br/> ||<span data-ttu-id="4ec38-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4ec38-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ec38-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="4ec38-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="4ec38-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4ec38-141">xsd:string</span></span>  <br/> |<span data-ttu-id="4ec38-142">opcional</span><span class="sxs-lookup"><span data-stu-id="4ec38-142">optional</span></span>  <br/> ||<span data-ttu-id="4ec38-143">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4ec38-143">Values of the xsd:string type.</span></span>  <br/> |
   

