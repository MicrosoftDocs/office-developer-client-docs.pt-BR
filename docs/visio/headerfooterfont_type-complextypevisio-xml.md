---
title: HeaderFooterFont_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541068"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="7c5e8-102">HeaderFooterFont_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="7c5e8-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7c5e8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7c5e8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c5e8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c5e8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c5e8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7c5e8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c5e8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c5e8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7c5e8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c5e8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7c5e8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7c5e8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7c5e8-110">Elements and attributes</span></span>

<span data-ttu-id="7c5e8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c5e8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7c5e8-112">Child elements</span></span>

<span data-ttu-id="7c5e8-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c5e8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c5e8-114">Attributes</span></span>

|<span data-ttu-id="7c5e8-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-115">**Attribute**</span></span>|<span data-ttu-id="7c5e8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-116">**Type**</span></span>|<span data-ttu-id="7c5e8-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-117">**Required**</span></span>|<span data-ttu-id="7c5e8-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-118">**Description**</span></span>|<span data-ttu-id="7c5e8-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7c5e8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c5e8-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="7c5e8-120">CharSet</span></span>  <br/> |<span data-ttu-id="7c5e8-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-122">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-122">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-123">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="7c5e8-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="7c5e8-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-126">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-126">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-128">Escape</span><span class="sxs-lookup"><span data-stu-id="7c5e8-128">Escapement</span></span>  <br/> |<span data-ttu-id="7c5e8-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7c5e8-129">xsd:int</span></span>  <br/> |<span data-ttu-id="7c5e8-130">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-130">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-131">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="7c5e8-132">FaceName</span></span>  <br/> |<span data-ttu-id="7c5e8-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7c5e8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="7c5e8-134">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-134">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-136">Altura</span><span class="sxs-lookup"><span data-stu-id="7c5e8-136">Height</span></span>  <br/> |<span data-ttu-id="7c5e8-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7c5e8-137">xsd:int</span></span>  <br/> |<span data-ttu-id="7c5e8-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-138">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-140">Itálico</span><span class="sxs-lookup"><span data-stu-id="7c5e8-140">Italic</span></span>  <br/> |<span data-ttu-id="7c5e8-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-142">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-142">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-143">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-144">Orientação</span><span class="sxs-lookup"><span data-stu-id="7c5e8-144">Orientation</span></span>  <br/> |<span data-ttu-id="7c5e8-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7c5e8-145">xsd:int</span></span>  <br/> |<span data-ttu-id="7c5e8-146">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-146">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-147">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="7c5e8-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="7c5e8-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-150">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-151">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="7c5e8-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="7c5e8-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-154">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-154">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-155">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-156">Qualidade</span><span class="sxs-lookup"><span data-stu-id="7c5e8-156">Quality</span></span>  <br/> |<span data-ttu-id="7c5e8-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-158">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-158">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-159">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="7c5e8-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="7c5e8-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-162">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-162">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-163">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-164">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="7c5e8-164">Underline</span></span>  <br/> |<span data-ttu-id="7c5e8-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7c5e8-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7c5e8-166">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-166">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-167">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-168">Peso</span><span class="sxs-lookup"><span data-stu-id="7c5e8-168">Weight</span></span>  <br/> |<span data-ttu-id="7c5e8-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7c5e8-169">xsd:int</span></span>  <br/> |<span data-ttu-id="7c5e8-170">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-170">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="7c5e8-172">Largura</span><span class="sxs-lookup"><span data-stu-id="7c5e8-172">Width</span></span>  <br/> |<span data-ttu-id="7c5e8-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="7c5e8-173">xsd:int</span></span>  <br/> |<span data-ttu-id="7c5e8-174">opcional</span><span class="sxs-lookup"><span data-stu-id="7c5e8-174">optional</span></span>  <br/> ||<span data-ttu-id="7c5e8-175">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="7c5e8-175">Values of the xsd:int type.</span></span>  <br/> |
   

