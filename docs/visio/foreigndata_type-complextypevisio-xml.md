---
title: ForeignData_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539860"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="7d1b9-102">ForeignData_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="7d1b9-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7d1b9-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7d1b9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d1b9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d1b9-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d1b9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7d1b9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d1b9-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d1b9-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7d1b9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d1b9-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7d1b9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7d1b9-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7d1b9-110">Elements and attributes</span></span>

<span data-ttu-id="7d1b9-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d1b9-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7d1b9-112">Child elements</span></span>

|<span data-ttu-id="7d1b9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-113">**Element**</span></span>|<span data-ttu-id="7d1b9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-114">**Type**</span></span>|<span data-ttu-id="7d1b9-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d1b9-116">Rel</span><span class="sxs-lookup"><span data-stu-id="7d1b9-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d1b9-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="7d1b9-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7d1b9-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d1b9-118">Attributes</span></span>

|<span data-ttu-id="7d1b9-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-119">**Attribute**</span></span>|<span data-ttu-id="7d1b9-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-120">**Type**</span></span>|<span data-ttu-id="7d1b9-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-121">**Required**</span></span>|<span data-ttu-id="7d1b9-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-122">**Description**</span></span>|<span data-ttu-id="7d1b9-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7d1b9-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d1b9-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="7d1b9-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="7d1b9-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7d1b9-125">xsd:double</span></span>  <br/> |<span data-ttu-id="7d1b9-126">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-126">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-127">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="7d1b9-128">CompressionType</span></span>  <br/> |<span data-ttu-id="7d1b9-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="7d1b9-129">xsd:token</span></span>  <br/> |<span data-ttu-id="7d1b9-130">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-130">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-131">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="7d1b9-132">ExtentX</span></span>  <br/> |<span data-ttu-id="7d1b9-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7d1b9-133">xsd:double</span></span>  <br/> |<span data-ttu-id="7d1b9-134">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-134">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-135">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="7d1b9-136">ExtentY</span></span>  <br/> |<span data-ttu-id="7d1b9-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7d1b9-137">xsd:double</span></span>  <br/> |<span data-ttu-id="7d1b9-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-138">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-139">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="7d1b9-140">ForeignType</span></span>  <br/> |<span data-ttu-id="7d1b9-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="7d1b9-141">xsd:token</span></span>  <br/> |<span data-ttu-id="7d1b9-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d1b9-142">required</span></span>  <br/> ||<span data-ttu-id="7d1b9-143">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="7d1b9-144">MappingMode</span></span>  <br/> |<span data-ttu-id="7d1b9-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7d1b9-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7d1b9-146">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-146">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="7d1b9-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="7d1b9-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7d1b9-149">xsd:double</span></span>  <br/> |<span data-ttu-id="7d1b9-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-150">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-151">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="7d1b9-152">ObjectType</span></span>  <br/> |<span data-ttu-id="7d1b9-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d1b9-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d1b9-154">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-154">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="7d1b9-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="7d1b9-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7d1b9-157">xsd:double</span></span>  <br/> |<span data-ttu-id="7d1b9-158">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-158">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-159">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7d1b9-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="7d1b9-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="7d1b9-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7d1b9-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7d1b9-162">opcional</span><span class="sxs-lookup"><span data-stu-id="7d1b9-162">optional</span></span>  <br/> ||<span data-ttu-id="7d1b9-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7d1b9-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

