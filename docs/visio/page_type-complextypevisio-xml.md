---
title: Page_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772442"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="f3cc2-102">Page_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f3cc2-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f3cc2-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="f3cc2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3cc2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f3cc2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f3cc2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f3cc2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f3cc2-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f3cc2-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f3cc2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3cc2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f3cc2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f3cc2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f3cc2-110">Elements and attributes</span></span>

<span data-ttu-id="f3cc2-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f3cc2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f3cc2-112">Child elements</span></span>

|<span data-ttu-id="f3cc2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-113">**Element**</span></span>|<span data-ttu-id="f3cc2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-114">**Type**</span></span>|<span data-ttu-id="f3cc2-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3cc2-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="f3cc2-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3cc2-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f3cc2-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f3cc2-118">Rel</span><span class="sxs-lookup"><span data-stu-id="f3cc2-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3cc2-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f3cc2-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f3cc2-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3cc2-120">Attributes</span></span>

|<span data-ttu-id="f3cc2-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-121">**Attribute**</span></span>|<span data-ttu-id="f3cc2-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-122">**Type**</span></span>|<span data-ttu-id="f3cc2-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-123">**Required**</span></span>|<span data-ttu-id="f3cc2-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-124">**Description**</span></span>|<span data-ttu-id="f3cc2-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f3cc2-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3cc2-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="f3cc2-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="f3cc2-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3cc2-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3cc2-128">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-128">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-130">Background</span><span class="sxs-lookup"><span data-stu-id="f3cc2-130">Background</span></span>  <br/> |<span data-ttu-id="f3cc2-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f3cc2-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3cc2-132">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-132">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="f3cc2-134">BackPage</span></span>  <br/> |<span data-ttu-id="f3cc2-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3cc2-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3cc2-136">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-136">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-138">ID</span><span class="sxs-lookup"><span data-stu-id="f3cc2-138">ID</span></span>  <br/> |<span data-ttu-id="f3cc2-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3cc2-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3cc2-140">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f3cc2-140">required</span></span>  <br/> ||<span data-ttu-id="f3cc2-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f3cc2-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="f3cc2-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f3cc2-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3cc2-144">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-144">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-145">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f3cc2-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f3cc2-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f3cc2-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3cc2-148">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-148">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-149">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-150">Nome</span><span class="sxs-lookup"><span data-stu-id="f3cc2-150">Name</span></span>  <br/> |<span data-ttu-id="f3cc2-151">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f3cc2-151">xsd:string</span></span>  <br/> |<span data-ttu-id="f3cc2-152">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-152">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-153">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-154">NameU</span><span class="sxs-lookup"><span data-stu-id="f3cc2-154">NameU</span></span>  <br/> |<span data-ttu-id="f3cc2-155">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f3cc2-155">xsd:string</span></span>  <br/> |<span data-ttu-id="f3cc2-156">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-156">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-157">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="f3cc2-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="f3cc2-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3cc2-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3cc2-160">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-160">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="f3cc2-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="f3cc2-163">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="f3cc2-163">xsd:double</span></span>  <br/> |<span data-ttu-id="f3cc2-164">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-164">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-165">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="f3cc2-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="f3cc2-167">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="f3cc2-167">xsd:double</span></span>  <br/> |<span data-ttu-id="f3cc2-168">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-168">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-169">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="f3cc2-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="f3cc2-170">ViewScale</span></span>  <br/> |<span data-ttu-id="f3cc2-171">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="f3cc2-171">xsd:double</span></span>  <br/> |<span data-ttu-id="f3cc2-172">opcional</span><span class="sxs-lookup"><span data-stu-id="f3cc2-172">optional</span></span>  <br/> ||<span data-ttu-id="f3cc2-173">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="f3cc2-173">Values of the xsd:double type.</span></span>  <br/> |
   

