---
title: HeaderFooterFont_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397244"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="fae0c-102">HeaderFooterFont_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fae0c-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fae0c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="fae0c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fae0c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fae0c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fae0c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fae0c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fae0c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fae0c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fae0c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="fae0c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fae0c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fae0c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fae0c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="fae0c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fae0c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fae0c-110">Elements and attributes</span></span>

<span data-ttu-id="fae0c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fae0c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fae0c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fae0c-112">Child elements</span></span>

<span data-ttu-id="fae0c-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fae0c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fae0c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="fae0c-114">Attributes</span></span>

|<span data-ttu-id="fae0c-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="fae0c-115">**Attribute**</span></span>|<span data-ttu-id="fae0c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fae0c-116">**Type**</span></span>|<span data-ttu-id="fae0c-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fae0c-117">**Required**</span></span>|<span data-ttu-id="fae0c-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fae0c-118">**Description**</span></span>|<span data-ttu-id="fae0c-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fae0c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fae0c-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="fae0c-120">CharSet</span></span>  <br/> |<span data-ttu-id="fae0c-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-122">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-122">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-123">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="fae0c-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="fae0c-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-126">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-128">Escape</span><span class="sxs-lookup"><span data-stu-id="fae0c-128">Escapement</span></span>  <br/> |<span data-ttu-id="fae0c-129">XSD:int</span><span class="sxs-lookup"><span data-stu-id="fae0c-129">xsd:int</span></span>  <br/> |<span data-ttu-id="fae0c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-130">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-131">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fae0c-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="fae0c-132">FaceName</span></span>  <br/> |<span data-ttu-id="fae0c-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fae0c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="fae0c-134">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-134">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fae0c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-136">Altura</span><span class="sxs-lookup"><span data-stu-id="fae0c-136">Height</span></span>  <br/> |<span data-ttu-id="fae0c-137">XSD:int</span><span class="sxs-lookup"><span data-stu-id="fae0c-137">xsd:int</span></span>  <br/> |<span data-ttu-id="fae0c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-138">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fae0c-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-140">Itálico</span><span class="sxs-lookup"><span data-stu-id="fae0c-140">Italic</span></span>  <br/> |<span data-ttu-id="fae0c-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-142">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-142">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-143">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="fae0c-144">Orientation</span></span>  <br/> |<span data-ttu-id="fae0c-145">XSD:int</span><span class="sxs-lookup"><span data-stu-id="fae0c-145">xsd:int</span></span>  <br/> |<span data-ttu-id="fae0c-146">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-146">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-147">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fae0c-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="fae0c-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="fae0c-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-150">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-150">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-151">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="fae0c-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="fae0c-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-154">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-154">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-155">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-156">Quality</span><span class="sxs-lookup"><span data-stu-id="fae0c-156">Quality</span></span>  <br/> |<span data-ttu-id="fae0c-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-158">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-158">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-159">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-160">Riscado</span><span class="sxs-lookup"><span data-stu-id="fae0c-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="fae0c-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-162">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-162">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-163">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-164">Sublinhado</span><span class="sxs-lookup"><span data-stu-id="fae0c-164">Underline</span></span>  <br/> |<span data-ttu-id="fae0c-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fae0c-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fae0c-166">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-166">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-167">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="fae0c-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-168">Peso</span><span class="sxs-lookup"><span data-stu-id="fae0c-168">Weight</span></span>  <br/> |<span data-ttu-id="fae0c-169">XSD:int</span><span class="sxs-lookup"><span data-stu-id="fae0c-169">xsd:int</span></span>  <br/> |<span data-ttu-id="fae0c-170">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-170">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-171">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fae0c-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fae0c-172">Largura</span><span class="sxs-lookup"><span data-stu-id="fae0c-172">Width</span></span>  <br/> |<span data-ttu-id="fae0c-173">XSD:int</span><span class="sxs-lookup"><span data-stu-id="fae0c-173">xsd:int</span></span>  <br/> |<span data-ttu-id="fae0c-174">opcional</span><span class="sxs-lookup"><span data-stu-id="fae0c-174">optional</span></span>  <br/> ||<span data-ttu-id="fae0c-175">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fae0c-175">Values of the xsd:int type.</span></span>  <br/> |
   

