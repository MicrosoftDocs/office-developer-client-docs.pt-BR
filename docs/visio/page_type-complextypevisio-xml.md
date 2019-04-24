---
title: Page_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334395"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="f250a-102">Page_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f250a-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f250a-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f250a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f250a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f250a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f250a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f250a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f250a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f250a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f250a-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f250a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f250a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f250a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f250a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f250a-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
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
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f250a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f250a-110">Elements and attributes</span></span>

<span data-ttu-id="f250a-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f250a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f250a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f250a-112">Child elements</span></span>

|<span data-ttu-id="f250a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f250a-113">**Element**</span></span>|<span data-ttu-id="f250a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f250a-114">**Type**</span></span>|<span data-ttu-id="f250a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f250a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f250a-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="f250a-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f250a-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f250a-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f250a-118">Rel</span><span class="sxs-lookup"><span data-stu-id="f250a-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f250a-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f250a-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f250a-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="f250a-120">Attributes</span></span>

|<span data-ttu-id="f250a-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f250a-121">**Attribute**</span></span>|<span data-ttu-id="f250a-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f250a-122">**Type**</span></span>|<span data-ttu-id="f250a-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f250a-123">**Required**</span></span>|<span data-ttu-id="f250a-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f250a-124">**Description**</span></span>|<span data-ttu-id="f250a-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f250a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f250a-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="f250a-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="f250a-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f250a-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f250a-128">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-128">optional</span></span>  <br/> ||<span data-ttu-id="f250a-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f250a-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f250a-130">Background</span><span class="sxs-lookup"><span data-stu-id="f250a-130">Background</span></span>  <br/> |<span data-ttu-id="f250a-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f250a-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f250a-132">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-132">optional</span></span>  <br/> ||<span data-ttu-id="f250a-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f250a-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f250a-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="f250a-134">BackPage</span></span>  <br/> |<span data-ttu-id="f250a-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f250a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f250a-136">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-136">optional</span></span>  <br/> ||<span data-ttu-id="f250a-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f250a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f250a-138">ID</span><span class="sxs-lookup"><span data-stu-id="f250a-138">ID</span></span>  <br/> |<span data-ttu-id="f250a-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f250a-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f250a-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f250a-140">required</span></span>  <br/> ||<span data-ttu-id="f250a-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f250a-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f250a-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f250a-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="f250a-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f250a-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f250a-144">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-144">optional</span></span>  <br/> ||<span data-ttu-id="f250a-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f250a-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f250a-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f250a-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f250a-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f250a-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f250a-148">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-148">optional</span></span>  <br/> ||<span data-ttu-id="f250a-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f250a-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f250a-150">Name</span><span class="sxs-lookup"><span data-stu-id="f250a-150">Name</span></span>  <br/> |<span data-ttu-id="f250a-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f250a-151">xsd:string</span></span>  <br/> |<span data-ttu-id="f250a-152">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-152">optional</span></span>  <br/> ||<span data-ttu-id="f250a-153">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f250a-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f250a-154">NameU</span><span class="sxs-lookup"><span data-stu-id="f250a-154">NameU</span></span>  <br/> |<span data-ttu-id="f250a-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f250a-155">xsd:string</span></span>  <br/> |<span data-ttu-id="f250a-156">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-156">optional</span></span>  <br/> ||<span data-ttu-id="f250a-157">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f250a-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f250a-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="f250a-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="f250a-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f250a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f250a-160">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-160">optional</span></span>  <br/> ||<span data-ttu-id="f250a-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f250a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f250a-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="f250a-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="f250a-163">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="f250a-163">xsd:double</span></span>  <br/> |<span data-ttu-id="f250a-164">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-164">optional</span></span>  <br/> ||<span data-ttu-id="f250a-165">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="f250a-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="f250a-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="f250a-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="f250a-167">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="f250a-167">xsd:double</span></span>  <br/> |<span data-ttu-id="f250a-168">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-168">optional</span></span>  <br/> ||<span data-ttu-id="f250a-169">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="f250a-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="f250a-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="f250a-170">ViewScale</span></span>  <br/> |<span data-ttu-id="f250a-171">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="f250a-171">xsd:double</span></span>  <br/> |<span data-ttu-id="f250a-172">opcional</span><span class="sxs-lookup"><span data-stu-id="f250a-172">optional</span></span>  <br/> ||<span data-ttu-id="f250a-173">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="f250a-173">Values of the xsd:double type.</span></span>  <br/> |
   

