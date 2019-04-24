---
title: ForeignData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346008"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="6d056-102">ForeignData_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6d056-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6d056-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="6d056-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d056-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d056-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d056-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d056-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d056-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6d056-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d056-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="6d056-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d056-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6d056-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d056-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6d056-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d056-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6d056-110">Elements and attributes</span></span>

<span data-ttu-id="6d056-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6d056-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d056-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6d056-112">Child elements</span></span>

|<span data-ttu-id="6d056-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d056-113">**Element**</span></span>|<span data-ttu-id="6d056-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6d056-114">**Type**</span></span>|<span data-ttu-id="6d056-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d056-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d056-116">Rel</span><span class="sxs-lookup"><span data-stu-id="6d056-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d056-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6d056-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6d056-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d056-118">Attributes</span></span>

|<span data-ttu-id="6d056-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6d056-119">**Attribute**</span></span>|<span data-ttu-id="6d056-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6d056-120">**Type**</span></span>|<span data-ttu-id="6d056-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6d056-121">**Required**</span></span>|<span data-ttu-id="6d056-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d056-122">**Description**</span></span>|<span data-ttu-id="6d056-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6d056-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d056-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="6d056-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="6d056-125">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="6d056-125">xsd:double</span></span>  <br/> |<span data-ttu-id="6d056-126">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-126">optional</span></span>  <br/> ||<span data-ttu-id="6d056-127">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="6d056-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6d056-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="6d056-128">CompressionType</span></span>  <br/> |<span data-ttu-id="6d056-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6d056-129">xsd:token</span></span>  <br/> |<span data-ttu-id="6d056-130">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-130">optional</span></span>  <br/> ||<span data-ttu-id="6d056-131">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="6d056-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6d056-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="6d056-132">ExtentX</span></span>  <br/> |<span data-ttu-id="6d056-133">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="6d056-133">xsd:double</span></span>  <br/> |<span data-ttu-id="6d056-134">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-134">optional</span></span>  <br/> ||<span data-ttu-id="6d056-135">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="6d056-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6d056-136">Extensão</span><span class="sxs-lookup"><span data-stu-id="6d056-136">ExtentY</span></span>  <br/> |<span data-ttu-id="6d056-137">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="6d056-137">xsd:double</span></span>  <br/> |<span data-ttu-id="6d056-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-138">optional</span></span>  <br/> ||<span data-ttu-id="6d056-139">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="6d056-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6d056-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="6d056-140">ForeignType</span></span>  <br/> |<span data-ttu-id="6d056-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6d056-141">xsd:token</span></span>  <br/> |<span data-ttu-id="6d056-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6d056-142">required</span></span>  <br/> ||<span data-ttu-id="6d056-143">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="6d056-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6d056-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="6d056-144">MappingMode</span></span>  <br/> |<span data-ttu-id="6d056-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6d056-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6d056-146">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-146">optional</span></span>  <br/> ||<span data-ttu-id="6d056-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6d056-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6d056-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="6d056-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="6d056-149">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="6d056-149">xsd:double</span></span>  <br/> |<span data-ttu-id="6d056-150">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-150">optional</span></span>  <br/> ||<span data-ttu-id="6d056-151">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="6d056-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6d056-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="6d056-152">ObjectType</span></span>  <br/> |<span data-ttu-id="6d056-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d056-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d056-154">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-154">optional</span></span>  <br/> ||<span data-ttu-id="6d056-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d056-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d056-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="6d056-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="6d056-157">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="6d056-157">xsd:double</span></span>  <br/> |<span data-ttu-id="6d056-158">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-158">optional</span></span>  <br/> ||<span data-ttu-id="6d056-159">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="6d056-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6d056-160">{AsIc</span><span class="sxs-lookup"><span data-stu-id="6d056-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="6d056-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6d056-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6d056-162">opcional</span><span class="sxs-lookup"><span data-stu-id="6d056-162">optional</span></span>  <br/> ||<span data-ttu-id="6d056-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6d056-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

