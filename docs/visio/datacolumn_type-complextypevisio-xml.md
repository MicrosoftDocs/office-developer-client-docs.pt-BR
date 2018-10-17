---
title: DataColumn_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388655"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="19fa8-102">DataColumn_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="19fa8-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="19fa8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="19fa8-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19fa8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19fa8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19fa8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="19fa8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19fa8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="19fa8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19fa8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="19fa8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19fa8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="19fa8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19fa8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="19fa8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19fa8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="19fa8-110">Elements and attributes</span></span>

<span data-ttu-id="19fa8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="19fa8-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19fa8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="19fa8-112">Child elements</span></span>

<span data-ttu-id="19fa8-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="19fa8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19fa8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="19fa8-114">Attributes</span></span>

|<span data-ttu-id="19fa8-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="19fa8-115">**Attribute**</span></span>|<span data-ttu-id="19fa8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19fa8-116">**Type**</span></span>|<span data-ttu-id="19fa8-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="19fa8-117">**Required**</span></span>|<span data-ttu-id="19fa8-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="19fa8-118">**Description**</span></span>|<span data-ttu-id="19fa8-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="19fa8-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19fa8-120">Calendário</span><span class="sxs-lookup"><span data-stu-id="19fa8-120">Calendar</span></span>  <br/> |<span data-ttu-id="19fa8-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19fa8-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19fa8-122">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-122">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-123">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19fa8-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="19fa8-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="19fa8-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19fa8-125">xsd:string</span></span>  <br/> |<span data-ttu-id="19fa8-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="19fa8-126">required</span></span>  <br/> ||<span data-ttu-id="19fa8-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19fa8-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-128">Moeda</span><span class="sxs-lookup"><span data-stu-id="19fa8-128">Currency</span></span>  <br/> |<span data-ttu-id="19fa8-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19fa8-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19fa8-130">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-130">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19fa8-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-132">DataType</span><span class="sxs-lookup"><span data-stu-id="19fa8-132">DataType</span></span>  <br/> |<span data-ttu-id="19fa8-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19fa8-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19fa8-134">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-134">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19fa8-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-136">Degree</span><span class="sxs-lookup"><span data-stu-id="19fa8-136">Degree</span></span>  <br/> |<span data-ttu-id="19fa8-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19fa8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19fa8-138">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-138">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19fa8-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="19fa8-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="19fa8-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19fa8-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19fa8-142">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-142">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19fa8-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="19fa8-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="19fa8-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19fa8-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19fa8-146">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-146">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19fa8-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-148">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="19fa8-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="19fa8-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19fa8-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19fa8-150">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-150">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-151">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19fa8-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-152">Rótulo</span><span class="sxs-lookup"><span data-stu-id="19fa8-152">Label</span></span>  <br/> |<span data-ttu-id="19fa8-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19fa8-153">xsd:string</span></span>  <br/> |<span data-ttu-id="19fa8-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="19fa8-154">required</span></span>  <br/> ||<span data-ttu-id="19fa8-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19fa8-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-156">LangID</span><span class="sxs-lookup"><span data-stu-id="19fa8-156">;LANGID</span></span>  <br/> |<span data-ttu-id="19fa8-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19fa8-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19fa8-158">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-158">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-159">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19fa8-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-160">Mapped</span><span class="sxs-lookup"><span data-stu-id="19fa8-160">Mapped</span></span>  <br/> |<span data-ttu-id="19fa8-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19fa8-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19fa8-162">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-162">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19fa8-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-164">Nome</span><span class="sxs-lookup"><span data-stu-id="19fa8-164">Name</span></span>  <br/> |<span data-ttu-id="19fa8-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19fa8-165">xsd:string</span></span>  <br/> |<span data-ttu-id="19fa8-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="19fa8-166">required</span></span>  <br/> ||<span data-ttu-id="19fa8-167">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19fa8-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="19fa8-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="19fa8-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19fa8-169">xsd:string</span></span>  <br/> |<span data-ttu-id="19fa8-170">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-170">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19fa8-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19fa8-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="19fa8-172">UnitType</span></span>  <br/> |<span data-ttu-id="19fa8-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19fa8-173">xsd:string</span></span>  <br/> |<span data-ttu-id="19fa8-174">opcional</span><span class="sxs-lookup"><span data-stu-id="19fa8-174">optional</span></span>  <br/> ||<span data-ttu-id="19fa8-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19fa8-175">Values of the xsd:string type.</span></span>  <br/> |
   

