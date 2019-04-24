---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335620"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="c4bc7-102">HeaderFooterFont_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c4bc7-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c4bc7-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c4bc7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4bc7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4bc7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4bc7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c4bc7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4bc7-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4bc7-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4bc7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4bc7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c4bc7-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c4bc7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c4bc7-110">Elements and attributes</span></span>

<span data-ttu-id="c4bc7-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4bc7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c4bc7-112">Child elements</span></span>

<span data-ttu-id="c4bc7-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4bc7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4bc7-114">Attributes</span></span>

|<span data-ttu-id="c4bc7-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-115">**Attribute**</span></span>|<span data-ttu-id="c4bc7-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-116">**Type**</span></span>|<span data-ttu-id="c4bc7-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-117">**Required**</span></span>|<span data-ttu-id="c4bc7-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-118">**Description**</span></span>|<span data-ttu-id="c4bc7-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c4bc7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4bc7-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="c4bc7-120">CharSet</span></span>  <br/> |<span data-ttu-id="c4bc7-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-122">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-122">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-123">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="c4bc7-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="c4bc7-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-126">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-126">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-128">Escape</span><span class="sxs-lookup"><span data-stu-id="c4bc7-128">Escapement</span></span>  <br/> |<span data-ttu-id="c4bc7-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="c4bc7-129">xsd:int</span></span>  <br/> |<span data-ttu-id="c4bc7-130">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-130">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-131">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="c4bc7-132">FaceName</span></span>  <br/> |<span data-ttu-id="c4bc7-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4bc7-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c4bc7-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-134">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-136">Altura</span><span class="sxs-lookup"><span data-stu-id="c4bc7-136">Height</span></span>  <br/> |<span data-ttu-id="c4bc7-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="c4bc7-137">xsd:int</span></span>  <br/> |<span data-ttu-id="c4bc7-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-138">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-140">Itálico</span><span class="sxs-lookup"><span data-stu-id="c4bc7-140">Italic</span></span>  <br/> |<span data-ttu-id="c4bc7-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-142">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-142">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-143">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-144">Orientação</span><span class="sxs-lookup"><span data-stu-id="c4bc7-144">Orientation</span></span>  <br/> |<span data-ttu-id="c4bc7-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="c4bc7-145">xsd:int</span></span>  <br/> |<span data-ttu-id="c4bc7-146">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-146">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-147">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-148">Precisão</span><span class="sxs-lookup"><span data-stu-id="c4bc7-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="c4bc7-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-150">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-150">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-151">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="c4bc7-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="c4bc7-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-154">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-154">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-155">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-156">Quality</span><span class="sxs-lookup"><span data-stu-id="c4bc7-156">Quality</span></span>  <br/> |<span data-ttu-id="c4bc7-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-158">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-158">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-159">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-160">Risca</span><span class="sxs-lookup"><span data-stu-id="c4bc7-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="c4bc7-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-162">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-162">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-163">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-164">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="c4bc7-164">Underline</span></span>  <br/> |<span data-ttu-id="c4bc7-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c4bc7-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c4bc7-166">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-166">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-167">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-168">Peso</span><span class="sxs-lookup"><span data-stu-id="c4bc7-168">Weight</span></span>  <br/> |<span data-ttu-id="c4bc7-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="c4bc7-169">xsd:int</span></span>  <br/> |<span data-ttu-id="c4bc7-170">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-170">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c4bc7-172">Largura</span><span class="sxs-lookup"><span data-stu-id="c4bc7-172">Width</span></span>  <br/> |<span data-ttu-id="c4bc7-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="c4bc7-173">xsd:int</span></span>  <br/> |<span data-ttu-id="c4bc7-174">opcional</span><span class="sxs-lookup"><span data-stu-id="c4bc7-174">optional</span></span>  <br/> ||<span data-ttu-id="c4bc7-175">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-175">Values of the xsd:int type.</span></span>  <br/> |
   

