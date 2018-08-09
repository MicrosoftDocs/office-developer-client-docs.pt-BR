---
title: DataColumn_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771648"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="d8011-102">DataColumn_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d8011-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d8011-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d8011-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8011-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8011-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8011-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8011-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8011-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8011-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8011-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d8011-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8011-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d8011-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8011-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d8011-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8011-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d8011-110">Elements and attributes</span></span>

<span data-ttu-id="d8011-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d8011-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8011-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8011-112">Child elements</span></span>

<span data-ttu-id="d8011-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d8011-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8011-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8011-114">Attributes</span></span>

|<span data-ttu-id="d8011-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8011-115">**Attribute**</span></span>|<span data-ttu-id="d8011-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8011-116">**Type**</span></span>|<span data-ttu-id="d8011-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d8011-117">**Required**</span></span>|<span data-ttu-id="d8011-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8011-118">**Description**</span></span>|<span data-ttu-id="d8011-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d8011-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8011-120">Calendário</span><span class="sxs-lookup"><span data-stu-id="d8011-120">Calendar</span></span>  <br/> |<span data-ttu-id="d8011-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d8011-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d8011-122">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-122">optional</span></span>  <br/> ||<span data-ttu-id="d8011-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d8011-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d8011-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="d8011-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="d8011-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8011-125">xsd:string</span></span>  <br/> |<span data-ttu-id="d8011-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8011-126">required</span></span>  <br/> ||<span data-ttu-id="d8011-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8011-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8011-128">Moeda</span><span class="sxs-lookup"><span data-stu-id="d8011-128">Currency</span></span>  <br/> |<span data-ttu-id="d8011-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d8011-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d8011-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-130">optional</span></span>  <br/> ||<span data-ttu-id="d8011-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d8011-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d8011-132">DataType</span><span class="sxs-lookup"><span data-stu-id="d8011-132">DataType</span></span>  <br/> |<span data-ttu-id="d8011-133">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d8011-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d8011-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-134">optional</span></span>  <br/> ||<span data-ttu-id="d8011-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d8011-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d8011-136">Degree</span><span class="sxs-lookup"><span data-stu-id="d8011-136">Degree</span></span>  <br/> |<span data-ttu-id="d8011-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8011-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8011-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-138">optional</span></span>  <br/> ||<span data-ttu-id="d8011-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8011-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8011-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="d8011-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="d8011-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8011-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8011-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-142">optional</span></span>  <br/> ||<span data-ttu-id="d8011-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8011-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8011-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="d8011-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="d8011-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8011-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8011-146">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-146">optional</span></span>  <br/> ||<span data-ttu-id="d8011-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8011-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8011-148">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="d8011-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="d8011-149">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d8011-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8011-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-150">optional</span></span>  <br/> ||<span data-ttu-id="d8011-151">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8011-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d8011-152">Rótulo</span><span class="sxs-lookup"><span data-stu-id="d8011-152">Label</span></span>  <br/> |<span data-ttu-id="d8011-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8011-153">xsd:string</span></span>  <br/> |<span data-ttu-id="d8011-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8011-154">required</span></span>  <br/> ||<span data-ttu-id="d8011-155">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8011-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8011-156">LangID</span><span class="sxs-lookup"><span data-stu-id="d8011-156">LangID</span></span>  <br/> |<span data-ttu-id="d8011-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8011-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8011-158">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-158">optional</span></span>  <br/> ||<span data-ttu-id="d8011-159">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8011-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8011-160">Mapeadas</span><span class="sxs-lookup"><span data-stu-id="d8011-160">Mapped</span></span>  <br/> |<span data-ttu-id="d8011-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d8011-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8011-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-162">optional</span></span>  <br/> ||<span data-ttu-id="d8011-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8011-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d8011-164">Nome</span><span class="sxs-lookup"><span data-stu-id="d8011-164">Name</span></span>  <br/> |<span data-ttu-id="d8011-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8011-165">xsd:string</span></span>  <br/> |<span data-ttu-id="d8011-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8011-166">required</span></span>  <br/> ||<span data-ttu-id="d8011-167">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8011-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8011-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="d8011-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="d8011-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8011-169">xsd:string</span></span>  <br/> |<span data-ttu-id="d8011-170">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-170">optional</span></span>  <br/> ||<span data-ttu-id="d8011-171">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8011-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8011-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="d8011-172">UnitType</span></span>  <br/> |<span data-ttu-id="d8011-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8011-173">xsd:string</span></span>  <br/> |<span data-ttu-id="d8011-174">opcional</span><span class="sxs-lookup"><span data-stu-id="d8011-174">optional</span></span>  <br/> ||<span data-ttu-id="d8011-175">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8011-175">Values of the xsd:string type.</span></span>  <br/> |
   

