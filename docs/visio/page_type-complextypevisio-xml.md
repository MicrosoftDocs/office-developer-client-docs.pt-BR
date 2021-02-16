---
title: Page_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537980"
---
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="5cc5f-102">Page_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="5cc5f-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5cc5f-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="5cc5f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cc5f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5cc5f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5cc5f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5cc5f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5cc5f-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5cc5f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5cc5f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5cc5f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5cc5f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5cc5f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5cc5f-110">Elements and attributes</span></span>

<span data-ttu-id="5cc5f-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5cc5f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5cc5f-112">Child elements</span></span>

|<span data-ttu-id="5cc5f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-113">**Element**</span></span>|<span data-ttu-id="5cc5f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-114">**Type**</span></span>|<span data-ttu-id="5cc5f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cc5f-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="5cc5f-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cc5f-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5cc5f-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5cc5f-118">Rel</span><span class="sxs-lookup"><span data-stu-id="5cc5f-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cc5f-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="5cc5f-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5cc5f-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="5cc5f-120">Attributes</span></span>

|<span data-ttu-id="5cc5f-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-121">**Attribute**</span></span>|<span data-ttu-id="5cc5f-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-122">**Type**</span></span>|<span data-ttu-id="5cc5f-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-123">**Required**</span></span>|<span data-ttu-id="5cc5f-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-124">**Description**</span></span>|<span data-ttu-id="5cc5f-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5cc5f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5cc5f-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="5cc5f-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="5cc5f-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5cc5f-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5cc5f-128">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-128">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-130">Histórico</span><span class="sxs-lookup"><span data-stu-id="5cc5f-130">Background</span></span>  <br/> |<span data-ttu-id="5cc5f-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5cc5f-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5cc5f-132">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-132">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="5cc5f-134">BackPage</span></span>  <br/> |<span data-ttu-id="5cc5f-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5cc5f-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5cc5f-136">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-136">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-138">ID</span><span class="sxs-lookup"><span data-stu-id="5cc5f-138">ID</span></span>  <br/> |<span data-ttu-id="5cc5f-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5cc5f-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5cc5f-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5cc5f-140">required</span></span>  <br/> ||<span data-ttu-id="5cc5f-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="5cc5f-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="5cc5f-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5cc5f-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5cc5f-144">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-144">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="5cc5f-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="5cc5f-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5cc5f-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5cc5f-148">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-148">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-150">Nome</span><span class="sxs-lookup"><span data-stu-id="5cc5f-150">Name</span></span>  <br/> |<span data-ttu-id="5cc5f-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5cc5f-151">xsd:string</span></span>  <br/> |<span data-ttu-id="5cc5f-152">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-152">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-153">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-154">NameU</span><span class="sxs-lookup"><span data-stu-id="5cc5f-154">NameU</span></span>  <br/> |<span data-ttu-id="5cc5f-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5cc5f-155">xsd:string</span></span>  <br/> |<span data-ttu-id="5cc5f-156">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-156">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-157">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="5cc5f-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="5cc5f-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5cc5f-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5cc5f-160">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-160">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="5cc5f-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="5cc5f-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5cc5f-163">xsd:double</span></span>  <br/> |<span data-ttu-id="5cc5f-164">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-164">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-165">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="5cc5f-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="5cc5f-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5cc5f-167">xsd:double</span></span>  <br/> |<span data-ttu-id="5cc5f-168">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-168">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-169">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="5cc5f-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="5cc5f-170">ViewScale</span></span>  <br/> |<span data-ttu-id="5cc5f-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5cc5f-171">xsd:double</span></span>  <br/> |<span data-ttu-id="5cc5f-172">opcional</span><span class="sxs-lookup"><span data-stu-id="5cc5f-172">optional</span></span>  <br/> ||<span data-ttu-id="5cc5f-173">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-173">Values of the xsd:double type.</span></span>  <br/> |
   

