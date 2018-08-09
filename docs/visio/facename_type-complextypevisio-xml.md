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
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="0c943-102">FaceName_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0c943-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0c943-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="0c943-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c943-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0c943-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c943-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0c943-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c943-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c943-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c943-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="0c943-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c943-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0c943-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c943-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0c943-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c943-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0c943-110">Elements and attributes</span></span>

<span data-ttu-id="0c943-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0c943-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c943-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0c943-112">Child elements</span></span>

<span data-ttu-id="0c943-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0c943-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c943-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c943-114">Attributes</span></span>

|<span data-ttu-id="0c943-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0c943-115">**Attribute**</span></span>|<span data-ttu-id="0c943-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0c943-116">**Type**</span></span>|<span data-ttu-id="0c943-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="0c943-117">**Required**</span></span>|<span data-ttu-id="0c943-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0c943-118">**Description**</span></span>|<span data-ttu-id="0c943-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="0c943-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c943-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="0c943-120">CharSets</span></span>  <br/> |<span data-ttu-id="0c943-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0c943-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0c943-122">opcional</span><span class="sxs-lookup"><span data-stu-id="0c943-122">optional</span></span>  <br/> ||<span data-ttu-id="0c943-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0c943-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c943-124">Sinalizadores</span><span class="sxs-lookup"><span data-stu-id="0c943-124">Flags</span></span>  <br/> |<span data-ttu-id="0c943-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c943-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c943-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0c943-126">optional</span></span>  <br/> ||<span data-ttu-id="0c943-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0c943-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c943-128">NameU</span><span class="sxs-lookup"><span data-stu-id="0c943-128">NameU</span></span>  <br/> |<span data-ttu-id="0c943-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0c943-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0c943-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="0c943-130">required</span></span>  <br/> ||<span data-ttu-id="0c943-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0c943-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c943-132">Panos</span><span class="sxs-lookup"><span data-stu-id="0c943-132">Panos</span></span>  <br/> |<span data-ttu-id="0c943-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0c943-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0c943-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0c943-134">optional</span></span>  <br/> ||<span data-ttu-id="0c943-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0c943-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c943-136">Panose</span><span class="sxs-lookup"><span data-stu-id="0c943-136">Panose</span></span>  <br/> |<span data-ttu-id="0c943-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0c943-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0c943-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0c943-138">optional</span></span>  <br/> ||<span data-ttu-id="0c943-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0c943-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c943-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="0c943-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="0c943-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0c943-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0c943-142">opcional</span><span class="sxs-lookup"><span data-stu-id="0c943-142">optional</span></span>  <br/> ||<span data-ttu-id="0c943-143">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0c943-143">Values of the xsd:string type.</span></span>  <br/> |
   

