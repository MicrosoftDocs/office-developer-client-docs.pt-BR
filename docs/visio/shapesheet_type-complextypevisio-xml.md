---
title: ShapeSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772917"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="8378c-102">ShapeSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8378c-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8378c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="8378c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8378c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8378c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8378c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8378c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8378c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8378c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8378c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="8378c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8378c-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8378c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="8378c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8378c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8378c-110">Elements and attributes</span></span>

<span data-ttu-id="8378c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8378c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8378c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8378c-112">Child elements</span></span>

|<span data-ttu-id="8378c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8378c-113">**Element**</span></span>|<span data-ttu-id="8378c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8378c-114">**Type**</span></span>|<span data-ttu-id="8378c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8378c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8378c-116">Data1</span><span class="sxs-lookup"><span data-stu-id="8378c-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8378c-118">Data2</span><span class="sxs-lookup"><span data-stu-id="8378c-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8378c-120">Data3</span><span class="sxs-lookup"><span data-stu-id="8378c-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8378c-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="8378c-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8378c-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="8378c-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8378c-126">Text</span><span class="sxs-lookup"><span data-stu-id="8378c-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8378c-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="8378c-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8378c-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="8378c-128">Attributes</span></span>

|<span data-ttu-id="8378c-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8378c-129">**Attribute**</span></span>|<span data-ttu-id="8378c-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8378c-130">**Type**</span></span>|<span data-ttu-id="8378c-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8378c-131">**Required**</span></span>|<span data-ttu-id="8378c-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8378c-132">**Description**</span></span>|<span data-ttu-id="8378c-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8378c-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8378c-134">DEL</span><span class="sxs-lookup"><span data-stu-id="8378c-134">Del</span></span>  <br/> |<span data-ttu-id="8378c-135">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8378c-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8378c-136">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-136">optional</span></span>  <br/> ||<span data-ttu-id="8378c-137">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8378c-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8378c-138">ID</span><span class="sxs-lookup"><span data-stu-id="8378c-138">ID</span></span>  <br/> |<span data-ttu-id="8378c-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8378c-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8378c-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8378c-140">required</span></span>  <br/> ||<span data-ttu-id="8378c-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8378c-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8378c-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="8378c-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="8378c-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8378c-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8378c-144">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-144">optional</span></span>  <br/> ||<span data-ttu-id="8378c-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8378c-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8378c-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="8378c-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="8378c-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8378c-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8378c-148">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-148">optional</span></span>  <br/> ||<span data-ttu-id="8378c-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8378c-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8378c-150">Master</span><span class="sxs-lookup"><span data-stu-id="8378c-150">Master</span></span>  <br/> |<span data-ttu-id="8378c-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8378c-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8378c-152">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-152">optional</span></span>  <br/> ||<span data-ttu-id="8378c-153">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8378c-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8378c-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="8378c-154">MasterShape</span></span>  <br/> |<span data-ttu-id="8378c-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8378c-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8378c-156">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-156">optional</span></span>  <br/> ||<span data-ttu-id="8378c-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8378c-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8378c-158">Nome</span><span class="sxs-lookup"><span data-stu-id="8378c-158">Name</span></span>  <br/> |<span data-ttu-id="8378c-159">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8378c-159">xsd:string</span></span>  <br/> |<span data-ttu-id="8378c-160">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-160">optional</span></span>  <br/> ||<span data-ttu-id="8378c-161">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8378c-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8378c-162">NameU</span><span class="sxs-lookup"><span data-stu-id="8378c-162">NameU</span></span>  <br/> |<span data-ttu-id="8378c-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8378c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8378c-164">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-164">optional</span></span>  <br/> ||<span data-ttu-id="8378c-165">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8378c-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8378c-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="8378c-166">OriginalID</span></span>  <br/> |<span data-ttu-id="8378c-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8378c-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8378c-168">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-168">optional</span></span>  <br/> ||<span data-ttu-id="8378c-169">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8378c-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8378c-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="8378c-170">Type</span></span>  <br/> |<span data-ttu-id="8378c-171">XSD:token</span><span class="sxs-lookup"><span data-stu-id="8378c-171">xsd:token</span></span>  <br/> |<span data-ttu-id="8378c-172">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-172">optional</span></span>  <br/> ||<span data-ttu-id="8378c-173">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="8378c-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="8378c-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="8378c-174">UniqueID</span></span>  <br/> |<span data-ttu-id="8378c-175">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8378c-175">xsd:string</span></span>  <br/> |<span data-ttu-id="8378c-176">opcional</span><span class="sxs-lookup"><span data-stu-id="8378c-176">optional</span></span>  <br/> ||<span data-ttu-id="8378c-177">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8378c-177">Values of the xsd:string type.</span></span>  <br/> |
   

