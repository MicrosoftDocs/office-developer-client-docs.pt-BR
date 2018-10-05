---
title: ShapeSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383629"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="a2e41-102">ShapeSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a2e41-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a2e41-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="a2e41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2e41-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2e41-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a2e41-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a2e41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a2e41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a2e41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a2e41-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="a2e41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a2e41-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2e41-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a2e41-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a2e41-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a2e41-110">Elements and attributes</span></span>

<span data-ttu-id="a2e41-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a2e41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2e41-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a2e41-112">Child elements</span></span>

|<span data-ttu-id="a2e41-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a2e41-113">**Element**</span></span>|<span data-ttu-id="a2e41-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2e41-114">**Type**</span></span>|<span data-ttu-id="a2e41-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2e41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a2e41-116">Data1</span><span class="sxs-lookup"><span data-stu-id="a2e41-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e41-118">Data2</span><span class="sxs-lookup"><span data-stu-id="a2e41-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e41-120">Data3</span><span class="sxs-lookup"><span data-stu-id="a2e41-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e41-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="a2e41-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e41-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="a2e41-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e41-126">Text</span><span class="sxs-lookup"><span data-stu-id="a2e41-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e41-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a2e41-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a2e41-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2e41-128">Attributes</span></span>

|<span data-ttu-id="a2e41-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a2e41-129">**Attribute**</span></span>|<span data-ttu-id="a2e41-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2e41-130">**Type**</span></span>|<span data-ttu-id="a2e41-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a2e41-131">**Required**</span></span>|<span data-ttu-id="a2e41-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2e41-132">**Description**</span></span>|<span data-ttu-id="a2e41-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a2e41-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2e41-134">DEL</span><span class="sxs-lookup"><span data-stu-id="a2e41-134">Del</span></span>  <br/> |<span data-ttu-id="a2e41-135">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e41-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2e41-136">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-136">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-137">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a2e41-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-138">ID</span><span class="sxs-lookup"><span data-stu-id="a2e41-138">ID</span></span>  <br/> |<span data-ttu-id="a2e41-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e41-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e41-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2e41-140">required</span></span>  <br/> ||<span data-ttu-id="a2e41-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e41-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a2e41-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="a2e41-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e41-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2e41-144">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-144">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a2e41-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a2e41-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a2e41-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e41-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2e41-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-148">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a2e41-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-150">Master</span><span class="sxs-lookup"><span data-stu-id="a2e41-150">Master</span></span>  <br/> |<span data-ttu-id="a2e41-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e41-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e41-152">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-152">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-153">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e41-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="a2e41-154">MasterShape</span></span>  <br/> |<span data-ttu-id="a2e41-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e41-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e41-156">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-156">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e41-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-158">Nome</span><span class="sxs-lookup"><span data-stu-id="a2e41-158">Name</span></span>  <br/> |<span data-ttu-id="a2e41-159">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a2e41-159">xsd:string</span></span>  <br/> |<span data-ttu-id="a2e41-160">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-160">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-161">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a2e41-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-162">NameU</span><span class="sxs-lookup"><span data-stu-id="a2e41-162">NameU</span></span>  <br/> |<span data-ttu-id="a2e41-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a2e41-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a2e41-164">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-164">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-165">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a2e41-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="a2e41-166">OriginalID</span></span>  <br/> |<span data-ttu-id="a2e41-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e41-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e41-168">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-168">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-169">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e41-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2e41-170">Type</span></span>  <br/> |<span data-ttu-id="a2e41-171">XSD:token</span><span class="sxs-lookup"><span data-stu-id="a2e41-171">xsd:token</span></span>  <br/> |<span data-ttu-id="a2e41-172">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-172">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-173">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a2e41-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a2e41-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="a2e41-174">UniqueID</span></span>  <br/> |<span data-ttu-id="a2e41-175">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a2e41-175">xsd:string</span></span>  <br/> |<span data-ttu-id="a2e41-176">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e41-176">optional</span></span>  <br/> ||<span data-ttu-id="a2e41-177">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a2e41-177">Values of the xsd:string type.</span></span>  <br/> |
   

