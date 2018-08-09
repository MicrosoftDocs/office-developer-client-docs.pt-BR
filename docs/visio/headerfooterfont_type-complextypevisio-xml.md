---
title: HeaderFooterFont_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772000"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="d8eb6-102">HeaderFooterFont_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d8eb6-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d8eb6-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d8eb6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8eb6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8eb6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8eb6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8eb6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8eb6-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8eb6-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d8eb6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8eb6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d8eb6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d8eb6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d8eb6-110">Elements and attributes</span></span>

<span data-ttu-id="d8eb6-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8eb6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8eb6-112">Child elements</span></span>

<span data-ttu-id="d8eb6-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8eb6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8eb6-114">Attributes</span></span>

|<span data-ttu-id="d8eb6-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-115">**Attribute**</span></span>|<span data-ttu-id="d8eb6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-116">**Type**</span></span>|<span data-ttu-id="d8eb6-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-117">**Required**</span></span>|<span data-ttu-id="d8eb6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-118">**Description**</span></span>|<span data-ttu-id="d8eb6-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d8eb6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8eb6-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="d8eb6-120">CharSet</span></span>  <br/> |<span data-ttu-id="d8eb6-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-122">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-122">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-123">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="d8eb6-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="d8eb6-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-126">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-128">Escape</span><span class="sxs-lookup"><span data-stu-id="d8eb6-128">Escapement</span></span>  <br/> |<span data-ttu-id="d8eb6-129">XSD:int</span><span class="sxs-lookup"><span data-stu-id="d8eb6-129">xsd:int</span></span>  <br/> |<span data-ttu-id="d8eb6-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-130">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-131">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="d8eb6-132">FaceName</span></span>  <br/> |<span data-ttu-id="d8eb6-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8eb6-133">xsd:string</span></span>  <br/> |<span data-ttu-id="d8eb6-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-134">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-136">Altura</span><span class="sxs-lookup"><span data-stu-id="d8eb6-136">Height</span></span>  <br/> |<span data-ttu-id="d8eb6-137">XSD:int</span><span class="sxs-lookup"><span data-stu-id="d8eb6-137">xsd:int</span></span>  <br/> |<span data-ttu-id="d8eb6-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-138">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-140">Itálico</span><span class="sxs-lookup"><span data-stu-id="d8eb6-140">Italic</span></span>  <br/> |<span data-ttu-id="d8eb6-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-142">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-143">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="d8eb6-144">Orientation</span></span>  <br/> |<span data-ttu-id="d8eb6-145">XSD:int</span><span class="sxs-lookup"><span data-stu-id="d8eb6-145">xsd:int</span></span>  <br/> |<span data-ttu-id="d8eb6-146">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-146">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-147">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="d8eb6-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="d8eb6-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-150">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-151">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="d8eb6-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="d8eb6-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-154">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-154">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-155">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-156">Quality</span><span class="sxs-lookup"><span data-stu-id="d8eb6-156">Quality</span></span>  <br/> |<span data-ttu-id="d8eb6-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-158">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-158">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-159">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-160">Riscado</span><span class="sxs-lookup"><span data-stu-id="d8eb6-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="d8eb6-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-162">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-163">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-164">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="d8eb6-164">Underline</span></span>  <br/> |<span data-ttu-id="d8eb6-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d8eb6-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d8eb6-166">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-166">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-167">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-168">Peso</span><span class="sxs-lookup"><span data-stu-id="d8eb6-168">Weight</span></span>  <br/> |<span data-ttu-id="d8eb6-169">XSD:int</span><span class="sxs-lookup"><span data-stu-id="d8eb6-169">xsd:int</span></span>  <br/> |<span data-ttu-id="d8eb6-170">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-170">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d8eb6-172">Largura</span><span class="sxs-lookup"><span data-stu-id="d8eb6-172">Width</span></span>  <br/> |<span data-ttu-id="d8eb6-173">XSD:int</span><span class="sxs-lookup"><span data-stu-id="d8eb6-173">xsd:int</span></span>  <br/> |<span data-ttu-id="d8eb6-174">opcional</span><span class="sxs-lookup"><span data-stu-id="d8eb6-174">optional</span></span>  <br/> ||<span data-ttu-id="d8eb6-175">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-175">Values of the xsd:int type.</span></span>  <br/> |
   

