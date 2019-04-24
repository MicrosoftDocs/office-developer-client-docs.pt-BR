---
title: DataColumn_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344699"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="bec4d-102">DataColumn_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bec4d-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bec4d-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="bec4d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bec4d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bec4d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bec4d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bec4d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bec4d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bec4d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bec4d-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="bec4d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bec4d-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bec4d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bec4d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bec4d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bec4d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bec4d-110">Elements and attributes</span></span>

<span data-ttu-id="bec4d-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bec4d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bec4d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bec4d-112">Child elements</span></span>

<span data-ttu-id="bec4d-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bec4d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bec4d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bec4d-114">Attributes</span></span>

|<span data-ttu-id="bec4d-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bec4d-115">**Attribute**</span></span>|<span data-ttu-id="bec4d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bec4d-116">**Type**</span></span>|<span data-ttu-id="bec4d-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bec4d-117">**Required**</span></span>|<span data-ttu-id="bec4d-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bec4d-118">**Description**</span></span>|<span data-ttu-id="bec4d-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bec4d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bec4d-120">Calendário</span><span class="sxs-lookup"><span data-stu-id="bec4d-120">Calendar</span></span>  <br/> |<span data-ttu-id="bec4d-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bec4d-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bec4d-122">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-122">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bec4d-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="bec4d-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="bec4d-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bec4d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bec4d-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bec4d-126">required</span></span>  <br/> ||<span data-ttu-id="bec4d-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bec4d-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-128">Moeda</span><span class="sxs-lookup"><span data-stu-id="bec4d-128">Currency</span></span>  <br/> |<span data-ttu-id="bec4d-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bec4d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bec4d-130">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-130">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bec4d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-132">DataType</span><span class="sxs-lookup"><span data-stu-id="bec4d-132">DataType</span></span>  <br/> |<span data-ttu-id="bec4d-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bec4d-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bec4d-134">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-134">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bec4d-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-136">Degree</span><span class="sxs-lookup"><span data-stu-id="bec4d-136">Degree</span></span>  <br/> |<span data-ttu-id="bec4d-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bec4d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bec4d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-138">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bec4d-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="bec4d-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="bec4d-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bec4d-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bec4d-142">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-142">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bec4d-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="bec4d-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="bec4d-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bec4d-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bec4d-146">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-146">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bec4d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-148">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="bec4d-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="bec4d-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="bec4d-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bec4d-150">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-150">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-151">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bec4d-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-152">Rótulo</span><span class="sxs-lookup"><span data-stu-id="bec4d-152">Label</span></span>  <br/> |<span data-ttu-id="bec4d-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bec4d-153">xsd:string</span></span>  <br/> |<span data-ttu-id="bec4d-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bec4d-154">required</span></span>  <br/> ||<span data-ttu-id="bec4d-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bec4d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-156">LangID</span><span class="sxs-lookup"><span data-stu-id="bec4d-156">LangID</span></span>  <br/> |<span data-ttu-id="bec4d-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bec4d-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bec4d-158">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-158">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-159">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bec4d-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-160">Mapped</span><span class="sxs-lookup"><span data-stu-id="bec4d-160">Mapped</span></span>  <br/> |<span data-ttu-id="bec4d-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="bec4d-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bec4d-162">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-162">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bec4d-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-164">Name</span><span class="sxs-lookup"><span data-stu-id="bec4d-164">Name</span></span>  <br/> |<span data-ttu-id="bec4d-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bec4d-165">xsd:string</span></span>  <br/> |<span data-ttu-id="bec4d-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bec4d-166">required</span></span>  <br/> ||<span data-ttu-id="bec4d-167">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bec4d-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="bec4d-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="bec4d-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bec4d-169">xsd:string</span></span>  <br/> |<span data-ttu-id="bec4d-170">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-170">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bec4d-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bec4d-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="bec4d-172">UnitType</span></span>  <br/> |<span data-ttu-id="bec4d-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bec4d-173">xsd:string</span></span>  <br/> |<span data-ttu-id="bec4d-174">opcional</span><span class="sxs-lookup"><span data-stu-id="bec4d-174">optional</span></span>  <br/> ||<span data-ttu-id="bec4d-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bec4d-175">Values of the xsd:string type.</span></span>  <br/> |
   

