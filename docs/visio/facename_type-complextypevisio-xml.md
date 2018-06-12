---
title: FaceName_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771835"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="f66ae-102">FaceName_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f66ae-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f66ae-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="f66ae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f66ae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f66ae-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f66ae-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f66ae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f66ae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f66ae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f66ae-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="f66ae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f66ae-108">None</span><span class="sxs-lookup"><span data-stu-id="f66ae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f66ae-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f66ae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f66ae-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f66ae-110">Elements and attributes</span></span>

<span data-ttu-id="f66ae-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f66ae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f66ae-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f66ae-112">Child elements</span></span>

<span data-ttu-id="f66ae-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f66ae-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f66ae-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f66ae-114">Attributes</span></span>

|<span data-ttu-id="f66ae-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f66ae-115">**Attribute**</span></span>|<span data-ttu-id="f66ae-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f66ae-116">**Type**</span></span>|<span data-ttu-id="f66ae-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f66ae-117">**Required**</span></span>|<span data-ttu-id="f66ae-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f66ae-118">**Description**</span></span>|<span data-ttu-id="f66ae-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f66ae-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f66ae-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="f66ae-120">CharSets</span></span>  <br/> |<span data-ttu-id="f66ae-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f66ae-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f66ae-122">opcional</span><span class="sxs-lookup"><span data-stu-id="f66ae-122">optional</span></span>  <br/> ||<span data-ttu-id="f66ae-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f66ae-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f66ae-124">Sinalizadores</span><span class="sxs-lookup"><span data-stu-id="f66ae-124">Flags</span></span>  <br/> |<span data-ttu-id="f66ae-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f66ae-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f66ae-126">opcional</span><span class="sxs-lookup"><span data-stu-id="f66ae-126">optional</span></span>  <br/> ||<span data-ttu-id="f66ae-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f66ae-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f66ae-128">NameU</span><span class="sxs-lookup"><span data-stu-id="f66ae-128">NameU</span></span>  <br/> |<span data-ttu-id="f66ae-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f66ae-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f66ae-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f66ae-130">required</span></span>  <br/> ||<span data-ttu-id="f66ae-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f66ae-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f66ae-132">Panos</span><span class="sxs-lookup"><span data-stu-id="f66ae-132">Panos</span></span>  <br/> |<span data-ttu-id="f66ae-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f66ae-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f66ae-134">opcional</span><span class="sxs-lookup"><span data-stu-id="f66ae-134">optional</span></span>  <br/> ||<span data-ttu-id="f66ae-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f66ae-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f66ae-136">Panose</span><span class="sxs-lookup"><span data-stu-id="f66ae-136">Panose</span></span>  <br/> |<span data-ttu-id="f66ae-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f66ae-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f66ae-138">opcional</span><span class="sxs-lookup"><span data-stu-id="f66ae-138">optional</span></span>  <br/> ||<span data-ttu-id="f66ae-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f66ae-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f66ae-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="f66ae-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="f66ae-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f66ae-141">xsd:string</span></span>  <br/> |<span data-ttu-id="f66ae-142">opcional</span><span class="sxs-lookup"><span data-stu-id="f66ae-142">optional</span></span>  <br/> ||<span data-ttu-id="f66ae-143">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f66ae-143">Values of the xsd:string type.</span></span>  <br/> |
   

