---
title: ForeignData_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771934"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="a014b-102">ForeignData_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a014b-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a014b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="a014b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a014b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a014b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a014b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a014b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a014b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a014b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a014b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="a014b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a014b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a014b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a014b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a014b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a014b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a014b-110">Elements and attributes</span></span>

<span data-ttu-id="a014b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a014b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a014b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a014b-112">Child elements</span></span>

|<span data-ttu-id="a014b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a014b-113">**Element**</span></span>|<span data-ttu-id="a014b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a014b-114">**Type**</span></span>|<span data-ttu-id="a014b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a014b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a014b-116">Rel</span><span class="sxs-lookup"><span data-stu-id="a014b-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a014b-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a014b-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a014b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="a014b-118">Attributes</span></span>

|<span data-ttu-id="a014b-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a014b-119">**Attribute**</span></span>|<span data-ttu-id="a014b-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a014b-120">**Type**</span></span>|<span data-ttu-id="a014b-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a014b-121">**Required**</span></span>|<span data-ttu-id="a014b-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a014b-122">**Description**</span></span>|<span data-ttu-id="a014b-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a014b-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a014b-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="a014b-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="a014b-125">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a014b-125">xsd:double</span></span>  <br/> |<span data-ttu-id="a014b-126">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-126">optional</span></span>  <br/> ||<span data-ttu-id="a014b-127">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a014b-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a014b-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="a014b-128">CompressionType</span></span>  <br/> |<span data-ttu-id="a014b-129">XSD:token</span><span class="sxs-lookup"><span data-stu-id="a014b-129">xsd:token</span></span>  <br/> |<span data-ttu-id="a014b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-130">optional</span></span>  <br/> ||<span data-ttu-id="a014b-131">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a014b-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a014b-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="a014b-132">ExtentX</span></span>  <br/> |<span data-ttu-id="a014b-133">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a014b-133">xsd:double</span></span>  <br/> |<span data-ttu-id="a014b-134">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-134">optional</span></span>  <br/> ||<span data-ttu-id="a014b-135">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a014b-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a014b-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="a014b-136">ExtentY</span></span>  <br/> |<span data-ttu-id="a014b-137">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a014b-137">xsd:double</span></span>  <br/> |<span data-ttu-id="a014b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-138">optional</span></span>  <br/> ||<span data-ttu-id="a014b-139">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a014b-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a014b-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="a014b-140">ForeignType</span></span>  <br/> |<span data-ttu-id="a014b-141">XSD:token</span><span class="sxs-lookup"><span data-stu-id="a014b-141">xsd:token</span></span>  <br/> |<span data-ttu-id="a014b-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a014b-142">required</span></span>  <br/> ||<span data-ttu-id="a014b-143">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a014b-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a014b-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="a014b-144">MappingMode</span></span>  <br/> |<span data-ttu-id="a014b-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a014b-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a014b-146">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-146">optional</span></span>  <br/> ||<span data-ttu-id="a014b-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a014b-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a014b-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="a014b-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="a014b-149">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a014b-149">xsd:double</span></span>  <br/> |<span data-ttu-id="a014b-150">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-150">optional</span></span>  <br/> ||<span data-ttu-id="a014b-151">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a014b-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a014b-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="a014b-152">ObjectType</span></span>  <br/> |<span data-ttu-id="a014b-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a014b-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a014b-154">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-154">optional</span></span>  <br/> ||<span data-ttu-id="a014b-155">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a014b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a014b-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="a014b-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="a014b-157">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a014b-157">xsd:double</span></span>  <br/> |<span data-ttu-id="a014b-158">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-158">optional</span></span>  <br/> ||<span data-ttu-id="a014b-159">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a014b-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a014b-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="a014b-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="a014b-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a014b-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a014b-162">opcional</span><span class="sxs-lookup"><span data-stu-id="a014b-162">optional</span></span>  <br/> ||<span data-ttu-id="a014b-163">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a014b-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

