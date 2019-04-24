---
title: ShapeSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349130"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="676b0-102">ShapeSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="676b0-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="676b0-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="676b0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="676b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="676b0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="676b0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="676b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="676b0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="676b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="676b0-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="676b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="676b0-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="676b0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="676b0-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="676b0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="676b0-110">Elements and attributes</span></span>

<span data-ttu-id="676b0-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="676b0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="676b0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="676b0-112">Child elements</span></span>

|<span data-ttu-id="676b0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="676b0-113">**Element**</span></span>|<span data-ttu-id="676b0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="676b0-114">**Type**</span></span>|<span data-ttu-id="676b0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="676b0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="676b0-116">Data1</span><span class="sxs-lookup"><span data-stu-id="676b0-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="676b0-118">Data2</span><span class="sxs-lookup"><span data-stu-id="676b0-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="676b0-120">Data3</span><span class="sxs-lookup"><span data-stu-id="676b0-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="676b0-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="676b0-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="676b0-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="676b0-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="676b0-126">Text</span><span class="sxs-lookup"><span data-stu-id="676b0-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="676b0-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="676b0-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="676b0-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="676b0-128">Attributes</span></span>

|<span data-ttu-id="676b0-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="676b0-129">**Attribute**</span></span>|<span data-ttu-id="676b0-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="676b0-130">**Type**</span></span>|<span data-ttu-id="676b0-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="676b0-131">**Required**</span></span>|<span data-ttu-id="676b0-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="676b0-132">**Description**</span></span>|<span data-ttu-id="676b0-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="676b0-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="676b0-134">Del</span><span class="sxs-lookup"><span data-stu-id="676b0-134">Del</span></span>  <br/> |<span data-ttu-id="676b0-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="676b0-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="676b0-136">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-136">optional</span></span>  <br/> ||<span data-ttu-id="676b0-137">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="676b0-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="676b0-138">ID</span><span class="sxs-lookup"><span data-stu-id="676b0-138">ID</span></span>  <br/> |<span data-ttu-id="676b0-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="676b0-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="676b0-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="676b0-140">required</span></span>  <br/> ||<span data-ttu-id="676b0-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="676b0-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="676b0-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="676b0-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="676b0-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="676b0-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="676b0-144">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-144">optional</span></span>  <br/> ||<span data-ttu-id="676b0-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="676b0-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="676b0-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="676b0-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="676b0-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="676b0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="676b0-148">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-148">optional</span></span>  <br/> ||<span data-ttu-id="676b0-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="676b0-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="676b0-150">Mestre</span><span class="sxs-lookup"><span data-stu-id="676b0-150">Master</span></span>  <br/> |<span data-ttu-id="676b0-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="676b0-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="676b0-152">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-152">optional</span></span>  <br/> ||<span data-ttu-id="676b0-153">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="676b0-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="676b0-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="676b0-154">MasterShape</span></span>  <br/> |<span data-ttu-id="676b0-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="676b0-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="676b0-156">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-156">optional</span></span>  <br/> ||<span data-ttu-id="676b0-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="676b0-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="676b0-158">Nome</span><span class="sxs-lookup"><span data-stu-id="676b0-158">Name</span></span>  <br/> |<span data-ttu-id="676b0-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="676b0-159">xsd:string</span></span>  <br/> |<span data-ttu-id="676b0-160">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-160">optional</span></span>  <br/> ||<span data-ttu-id="676b0-161">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="676b0-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="676b0-162">NameU</span><span class="sxs-lookup"><span data-stu-id="676b0-162">NameU</span></span>  <br/> |<span data-ttu-id="676b0-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="676b0-163">xsd:string</span></span>  <br/> |<span data-ttu-id="676b0-164">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-164">optional</span></span>  <br/> ||<span data-ttu-id="676b0-165">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="676b0-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="676b0-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="676b0-166">OriginalID</span></span>  <br/> |<span data-ttu-id="676b0-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="676b0-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="676b0-168">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-168">optional</span></span>  <br/> ||<span data-ttu-id="676b0-169">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="676b0-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="676b0-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="676b0-170">Type</span></span>  <br/> |<span data-ttu-id="676b0-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="676b0-171">xsd:token</span></span>  <br/> |<span data-ttu-id="676b0-172">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-172">optional</span></span>  <br/> ||<span data-ttu-id="676b0-173">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="676b0-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="676b0-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="676b0-174">UniqueID</span></span>  <br/> |<span data-ttu-id="676b0-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="676b0-175">xsd:string</span></span>  <br/> |<span data-ttu-id="676b0-176">opcional</span><span class="sxs-lookup"><span data-stu-id="676b0-176">optional</span></span>  <br/> ||<span data-ttu-id="676b0-177">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="676b0-177">Values of the xsd:string type.</span></span>  <br/> |
   

