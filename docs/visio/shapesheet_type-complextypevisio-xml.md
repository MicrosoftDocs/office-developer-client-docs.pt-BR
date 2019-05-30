---
title: ShapeSheet_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542055"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="aab04-102">ShapeSheet_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="aab04-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aab04-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="aab04-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aab04-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aab04-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aab04-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aab04-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aab04-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aab04-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aab04-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="aab04-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aab04-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aab04-109">Definição</span><span class="sxs-lookup"><span data-stu-id="aab04-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="aab04-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="aab04-110">Elements and attributes</span></span>

<span data-ttu-id="aab04-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="aab04-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aab04-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aab04-112">Child elements</span></span>

|<span data-ttu-id="aab04-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aab04-113">**Element**</span></span>|<span data-ttu-id="aab04-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aab04-114">**Type**</span></span>|<span data-ttu-id="aab04-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aab04-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aab04-116">Data1</span><span class="sxs-lookup"><span data-stu-id="aab04-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aab04-118">Data2</span><span class="sxs-lookup"><span data-stu-id="aab04-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aab04-120">Data3</span><span class="sxs-lookup"><span data-stu-id="aab04-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aab04-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="aab04-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aab04-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="aab04-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aab04-126">Text</span><span class="sxs-lookup"><span data-stu-id="aab04-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab04-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="aab04-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aab04-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="aab04-128">Attributes</span></span>

|<span data-ttu-id="aab04-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="aab04-129">**Attribute**</span></span>|<span data-ttu-id="aab04-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aab04-130">**Type**</span></span>|<span data-ttu-id="aab04-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="aab04-131">**Required**</span></span>|<span data-ttu-id="aab04-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aab04-132">**Description**</span></span>|<span data-ttu-id="aab04-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="aab04-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aab04-134">Del</span><span class="sxs-lookup"><span data-stu-id="aab04-134">Del</span></span>  <br/> |<span data-ttu-id="aab04-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aab04-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aab04-136">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-136">optional</span></span>  <br/> ||<span data-ttu-id="aab04-137">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aab04-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aab04-138">ID</span><span class="sxs-lookup"><span data-stu-id="aab04-138">ID</span></span>  <br/> |<span data-ttu-id="aab04-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aab04-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aab04-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="aab04-140">required</span></span>  <br/> ||<span data-ttu-id="aab04-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aab04-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aab04-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="aab04-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="aab04-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aab04-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aab04-144">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-144">optional</span></span>  <br/> ||<span data-ttu-id="aab04-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aab04-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aab04-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="aab04-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="aab04-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aab04-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aab04-148">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-148">optional</span></span>  <br/> ||<span data-ttu-id="aab04-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aab04-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aab04-150">Mestre</span><span class="sxs-lookup"><span data-stu-id="aab04-150">Master</span></span>  <br/> |<span data-ttu-id="aab04-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aab04-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aab04-152">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-152">optional</span></span>  <br/> ||<span data-ttu-id="aab04-153">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aab04-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aab04-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="aab04-154">MasterShape</span></span>  <br/> |<span data-ttu-id="aab04-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aab04-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aab04-156">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-156">optional</span></span>  <br/> ||<span data-ttu-id="aab04-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aab04-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aab04-158">Nome</span><span class="sxs-lookup"><span data-stu-id="aab04-158">Name</span></span>  <br/> |<span data-ttu-id="aab04-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aab04-159">xsd:string</span></span>  <br/> |<span data-ttu-id="aab04-160">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-160">optional</span></span>  <br/> ||<span data-ttu-id="aab04-161">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="aab04-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aab04-162">NameU</span><span class="sxs-lookup"><span data-stu-id="aab04-162">NameU</span></span>  <br/> |<span data-ttu-id="aab04-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aab04-163">xsd:string</span></span>  <br/> |<span data-ttu-id="aab04-164">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-164">optional</span></span>  <br/> ||<span data-ttu-id="aab04-165">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="aab04-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aab04-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="aab04-166">OriginalID</span></span>  <br/> |<span data-ttu-id="aab04-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aab04-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aab04-168">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-168">optional</span></span>  <br/> ||<span data-ttu-id="aab04-169">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aab04-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aab04-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="aab04-170">Type</span></span>  <br/> |<span data-ttu-id="aab04-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="aab04-171">xsd:token</span></span>  <br/> |<span data-ttu-id="aab04-172">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-172">optional</span></span>  <br/> ||<span data-ttu-id="aab04-173">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="aab04-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="aab04-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="aab04-174">UniqueID</span></span>  <br/> |<span data-ttu-id="aab04-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aab04-175">xsd:string</span></span>  <br/> |<span data-ttu-id="aab04-176">opcional</span><span class="sxs-lookup"><span data-stu-id="aab04-176">optional</span></span>  <br/> ||<span data-ttu-id="aab04-177">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="aab04-177">Values of the xsd:string type.</span></span>  <br/> |
   

