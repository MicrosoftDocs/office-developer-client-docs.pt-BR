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
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="8e143-102">HeaderFooterFont_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="8e143-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8e143-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="8e143-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e143-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8e143-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8e143-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8e143-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8e143-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8e143-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8e143-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="8e143-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8e143-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8e143-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e143-109">Definição</span><span class="sxs-lookup"><span data-stu-id="8e143-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8e143-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8e143-110">Elements and attributes</span></span>

<span data-ttu-id="8e143-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8e143-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8e143-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8e143-112">Child elements</span></span>

<span data-ttu-id="8e143-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8e143-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e143-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e143-114">Attributes</span></span>

|<span data-ttu-id="8e143-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8e143-115">**Attribute**</span></span>|<span data-ttu-id="8e143-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e143-116">**Type**</span></span>|<span data-ttu-id="8e143-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8e143-117">**Required**</span></span>|<span data-ttu-id="8e143-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e143-118">**Description**</span></span>|<span data-ttu-id="8e143-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8e143-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8e143-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="8e143-120">CharSet</span></span>  <br/> |<span data-ttu-id="8e143-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-122">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-122">optional</span></span>  <br/> ||<span data-ttu-id="8e143-123">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="8e143-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="8e143-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-126">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-126">optional</span></span>  <br/> ||<span data-ttu-id="8e143-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-128">Escape</span><span class="sxs-lookup"><span data-stu-id="8e143-128">Escapement</span></span>  <br/> |<span data-ttu-id="8e143-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="8e143-129">xsd:int</span></span>  <br/> |<span data-ttu-id="8e143-130">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-130">optional</span></span>  <br/> ||<span data-ttu-id="8e143-131">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="8e143-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8e143-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="8e143-132">FaceName</span></span>  <br/> |<span data-ttu-id="8e143-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e143-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8e143-134">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-134">optional</span></span>  <br/> ||<span data-ttu-id="8e143-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8e143-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8e143-136">Altura</span><span class="sxs-lookup"><span data-stu-id="8e143-136">Height</span></span>  <br/> |<span data-ttu-id="8e143-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="8e143-137">xsd:int</span></span>  <br/> |<span data-ttu-id="8e143-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-138">optional</span></span>  <br/> ||<span data-ttu-id="8e143-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="8e143-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8e143-140">Itálico</span><span class="sxs-lookup"><span data-stu-id="8e143-140">Italic</span></span>  <br/> |<span data-ttu-id="8e143-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-142">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-142">optional</span></span>  <br/> ||<span data-ttu-id="8e143-143">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-144">Orientação</span><span class="sxs-lookup"><span data-stu-id="8e143-144">Orientation</span></span>  <br/> |<span data-ttu-id="8e143-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="8e143-145">xsd:int</span></span>  <br/> |<span data-ttu-id="8e143-146">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-146">optional</span></span>  <br/> ||<span data-ttu-id="8e143-147">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="8e143-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8e143-148">Precisão</span><span class="sxs-lookup"><span data-stu-id="8e143-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="8e143-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-150">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-150">optional</span></span>  <br/> ||<span data-ttu-id="8e143-151">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="8e143-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="8e143-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-154">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-154">optional</span></span>  <br/> ||<span data-ttu-id="8e143-155">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-156">Quality</span><span class="sxs-lookup"><span data-stu-id="8e143-156">Quality</span></span>  <br/> |<span data-ttu-id="8e143-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-158">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-158">optional</span></span>  <br/> ||<span data-ttu-id="8e143-159">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-160">Risca</span><span class="sxs-lookup"><span data-stu-id="8e143-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="8e143-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-162">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-162">optional</span></span>  <br/> ||<span data-ttu-id="8e143-163">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-164">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="8e143-164">Underline</span></span>  <br/> |<span data-ttu-id="8e143-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8e143-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8e143-166">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-166">optional</span></span>  <br/> ||<span data-ttu-id="8e143-167">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="8e143-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8e143-168">Peso</span><span class="sxs-lookup"><span data-stu-id="8e143-168">Weight</span></span>  <br/> |<span data-ttu-id="8e143-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="8e143-169">xsd:int</span></span>  <br/> |<span data-ttu-id="8e143-170">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-170">optional</span></span>  <br/> ||<span data-ttu-id="8e143-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="8e143-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8e143-172">Largura</span><span class="sxs-lookup"><span data-stu-id="8e143-172">Width</span></span>  <br/> |<span data-ttu-id="8e143-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="8e143-173">xsd:int</span></span>  <br/> |<span data-ttu-id="8e143-174">opcional</span><span class="sxs-lookup"><span data-stu-id="8e143-174">optional</span></span>  <br/> ||<span data-ttu-id="8e143-175">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="8e143-175">Values of the xsd:int type.</span></span>  <br/> |
   

