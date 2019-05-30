---
title: DataColumn_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541208"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="75975-102">DataColumn_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="75975-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="75975-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="75975-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75975-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75975-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="75975-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="75975-105">**Schema file**</span></span> <br/> |<span data-ttu-id="75975-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="75975-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="75975-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="75975-107">**Extension base**</span></span> <br/> |<span data-ttu-id="75975-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75975-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75975-109">Definição</span><span class="sxs-lookup"><span data-stu-id="75975-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="75975-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="75975-110">Elements and attributes</span></span>

<span data-ttu-id="75975-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="75975-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75975-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="75975-112">Child elements</span></span>

<span data-ttu-id="75975-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="75975-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75975-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="75975-114">Attributes</span></span>

|<span data-ttu-id="75975-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="75975-115">**Attribute**</span></span>|<span data-ttu-id="75975-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75975-116">**Type**</span></span>|<span data-ttu-id="75975-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="75975-117">**Required**</span></span>|<span data-ttu-id="75975-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75975-118">**Description**</span></span>|<span data-ttu-id="75975-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="75975-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75975-120">Calendário</span><span class="sxs-lookup"><span data-stu-id="75975-120">Calendar</span></span>  <br/> |<span data-ttu-id="75975-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="75975-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="75975-122">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-122">optional</span></span>  <br/> ||<span data-ttu-id="75975-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="75975-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="75975-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="75975-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="75975-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75975-125">xsd:string</span></span>  <br/> |<span data-ttu-id="75975-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="75975-126">required</span></span>  <br/> ||<span data-ttu-id="75975-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75975-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75975-128">Moeda</span><span class="sxs-lookup"><span data-stu-id="75975-128">Currency</span></span>  <br/> |<span data-ttu-id="75975-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="75975-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="75975-130">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-130">optional</span></span>  <br/> ||<span data-ttu-id="75975-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="75975-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="75975-132">DataType</span><span class="sxs-lookup"><span data-stu-id="75975-132">DataType</span></span>  <br/> |<span data-ttu-id="75975-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="75975-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="75975-134">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-134">optional</span></span>  <br/> ||<span data-ttu-id="75975-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="75975-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="75975-136">Degree</span><span class="sxs-lookup"><span data-stu-id="75975-136">Degree</span></span>  <br/> |<span data-ttu-id="75975-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="75975-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75975-138">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-138">optional</span></span>  <br/> ||<span data-ttu-id="75975-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="75975-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75975-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="75975-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="75975-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="75975-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75975-142">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-142">optional</span></span>  <br/> ||<span data-ttu-id="75975-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="75975-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75975-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="75975-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="75975-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="75975-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75975-146">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-146">optional</span></span>  <br/> ||<span data-ttu-id="75975-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="75975-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75975-148">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="75975-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="75975-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="75975-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="75975-150">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-150">optional</span></span>  <br/> ||<span data-ttu-id="75975-151">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="75975-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="75975-152">Rótulo</span><span class="sxs-lookup"><span data-stu-id="75975-152">Label</span></span>  <br/> |<span data-ttu-id="75975-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75975-153">xsd:string</span></span>  <br/> |<span data-ttu-id="75975-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="75975-154">required</span></span>  <br/> ||<span data-ttu-id="75975-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75975-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75975-156">LangID</span><span class="sxs-lookup"><span data-stu-id="75975-156">LangID</span></span>  <br/> |<span data-ttu-id="75975-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="75975-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75975-158">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-158">optional</span></span>  <br/> ||<span data-ttu-id="75975-159">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="75975-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75975-160">Mapped</span><span class="sxs-lookup"><span data-stu-id="75975-160">Mapped</span></span>  <br/> |<span data-ttu-id="75975-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="75975-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="75975-162">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-162">optional</span></span>  <br/> ||<span data-ttu-id="75975-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="75975-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="75975-164">Nome</span><span class="sxs-lookup"><span data-stu-id="75975-164">Name</span></span>  <br/> |<span data-ttu-id="75975-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75975-165">xsd:string</span></span>  <br/> |<span data-ttu-id="75975-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="75975-166">required</span></span>  <br/> ||<span data-ttu-id="75975-167">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75975-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75975-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="75975-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="75975-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75975-169">xsd:string</span></span>  <br/> |<span data-ttu-id="75975-170">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-170">optional</span></span>  <br/> ||<span data-ttu-id="75975-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75975-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75975-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="75975-172">UnitType</span></span>  <br/> |<span data-ttu-id="75975-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75975-173">xsd:string</span></span>  <br/> |<span data-ttu-id="75975-174">opcional</span><span class="sxs-lookup"><span data-stu-id="75975-174">optional</span></span>  <br/> ||<span data-ttu-id="75975-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75975-175">Values of the xsd:string type.</span></span>  <br/> |
   

