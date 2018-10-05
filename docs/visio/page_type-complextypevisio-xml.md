---
title: Page_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401549"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="69ec0-102">Page_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="69ec0-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="69ec0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="69ec0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69ec0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69ec0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69ec0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="69ec0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69ec0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="69ec0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69ec0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="69ec0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69ec0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="69ec0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69ec0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="69ec0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="69ec0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="69ec0-110">Elements and attributes</span></span>

<span data-ttu-id="69ec0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="69ec0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69ec0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="69ec0-112">Child elements</span></span>

|<span data-ttu-id="69ec0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="69ec0-113">**Element**</span></span>|<span data-ttu-id="69ec0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="69ec0-114">**Type**</span></span>|<span data-ttu-id="69ec0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69ec0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69ec0-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="69ec0-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69ec0-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="69ec0-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69ec0-118">Rel</span><span class="sxs-lookup"><span data-stu-id="69ec0-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69ec0-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="69ec0-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69ec0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="69ec0-120">Attributes</span></span>

|<span data-ttu-id="69ec0-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="69ec0-121">**Attribute**</span></span>|<span data-ttu-id="69ec0-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="69ec0-122">**Type**</span></span>|<span data-ttu-id="69ec0-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="69ec0-123">**Required**</span></span>|<span data-ttu-id="69ec0-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69ec0-124">**Description**</span></span>|<span data-ttu-id="69ec0-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="69ec0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69ec0-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="69ec0-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="69ec0-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69ec0-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69ec0-128">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-128">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69ec0-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-130">Background</span><span class="sxs-lookup"><span data-stu-id="69ec0-130">Background</span></span>  <br/> |<span data-ttu-id="69ec0-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="69ec0-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69ec0-132">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-132">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="69ec0-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="69ec0-134">BackPage</span></span>  <br/> |<span data-ttu-id="69ec0-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69ec0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69ec0-136">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-136">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69ec0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-138">ID</span><span class="sxs-lookup"><span data-stu-id="69ec0-138">ID</span></span>  <br/> |<span data-ttu-id="69ec0-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69ec0-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69ec0-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="69ec0-140">required</span></span>  <br/> ||<span data-ttu-id="69ec0-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69ec0-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="69ec0-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="69ec0-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="69ec0-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69ec0-144">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-144">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="69ec0-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="69ec0-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="69ec0-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="69ec0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69ec0-148">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-148">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="69ec0-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-150">Nome</span><span class="sxs-lookup"><span data-stu-id="69ec0-150">Name</span></span>  <br/> |<span data-ttu-id="69ec0-151">XSD: String</span><span class="sxs-lookup"><span data-stu-id="69ec0-151">xsd:string</span></span>  <br/> |<span data-ttu-id="69ec0-152">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-152">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-153">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69ec0-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-154">NameU</span><span class="sxs-lookup"><span data-stu-id="69ec0-154">NameU</span></span>  <br/> |<span data-ttu-id="69ec0-155">XSD: String</span><span class="sxs-lookup"><span data-stu-id="69ec0-155">xsd:string</span></span>  <br/> |<span data-ttu-id="69ec0-156">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-156">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-157">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69ec0-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="69ec0-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="69ec0-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69ec0-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69ec0-160">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-160">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69ec0-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="69ec0-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="69ec0-163">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="69ec0-163">xsd:double</span></span>  <br/> |<span data-ttu-id="69ec0-164">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-164">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-165">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="69ec0-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="69ec0-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="69ec0-167">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="69ec0-167">xsd:double</span></span>  <br/> |<span data-ttu-id="69ec0-168">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-168">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-169">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="69ec0-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69ec0-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="69ec0-170">ViewScale</span></span>  <br/> |<span data-ttu-id="69ec0-171">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="69ec0-171">xsd:double</span></span>  <br/> |<span data-ttu-id="69ec0-172">opcional</span><span class="sxs-lookup"><span data-stu-id="69ec0-172">optional</span></span>  <br/> ||<span data-ttu-id="69ec0-173">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="69ec0-173">Values of the xsd:double type.</span></span>  <br/> |
   

