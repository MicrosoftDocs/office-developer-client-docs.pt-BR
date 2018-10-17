---
title: DocumentSettings_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 704591a2bf03f3eaf4d93b167475a8bae286da3e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384672"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="23b15-102">DocumentSettings_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="23b15-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23b15-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="23b15-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23b15-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="23b15-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23b15-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="23b15-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23b15-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23b15-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23b15-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="23b15-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23b15-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="23b15-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23b15-109">Definição</span><span class="sxs-lookup"><span data-stu-id="23b15-109">Definition</span></span>

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23b15-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="23b15-110">Elements and attributes</span></span>

<span data-ttu-id="23b15-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="23b15-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23b15-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="23b15-112">Child elements</span></span>

|<span data-ttu-id="23b15-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="23b15-113">**Element**</span></span>|<span data-ttu-id="23b15-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="23b15-114">**Type**</span></span>|<span data-ttu-id="23b15-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23b15-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23b15-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="23b15-116">AttachedToolbars element</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-117">AttachedToolbars_Type complexType</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="23b15-118">CustomMenusFile element</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-119">CustomMenusFile_Type complexType</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="23b15-120">CustomToolbarsFile element</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-121">CustomToolbarsFile_Type complexType</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="23b15-122">DynamicGridEnabled Property</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-123">DynamicGridEnabled_Type complexType</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="23b15-124">GlueSettings Property</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-125">GlueSettings_Type complexType</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="23b15-126">ProtectBkgnds element</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-127">ProtectBkgnds_Type complexType</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="23b15-128">ProtectMasters element</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-129">ProtectMasters_Type complexType</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="23b15-130">ProtectShapes element</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-131">ProtectShapes_Type complexType</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="23b15-132">ProtectStyles element</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-133">ProtectStyles_Type complexType</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="23b15-134">SnapAngles Property</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-135">SnapAngles_Type complexType</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="23b15-136">SnapExtensions Property</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-137">SnapExtensions_Type complexType</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23b15-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="23b15-138">SnapSettings Property</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23b15-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="23b15-139">SnapSettings_Type complexType</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23b15-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="23b15-140">Attributes</span></span>

|<span data-ttu-id="23b15-141">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="23b15-141">**Attribute**</span></span>|<span data-ttu-id="23b15-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="23b15-142">**Type**</span></span>|<span data-ttu-id="23b15-143">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="23b15-143">**Required**</span></span>|<span data-ttu-id="23b15-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23b15-144">**Description**</span></span>|<span data-ttu-id="23b15-145">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="23b15-145">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="23b15-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="23b15-146">DefaultFillStyle Property</span></span>  <br/> |<span data-ttu-id="23b15-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23b15-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23b15-148">opcional</span><span class="sxs-lookup"><span data-stu-id="23b15-148">optional</span></span>  <br/> ||<span data-ttu-id="23b15-149">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="23b15-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="23b15-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="23b15-150">DefaultGuideStyle Property</span></span>  <br/> |<span data-ttu-id="23b15-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23b15-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23b15-152">opcional</span><span class="sxs-lookup"><span data-stu-id="23b15-152">optional</span></span>  <br/> ||<span data-ttu-id="23b15-153">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="23b15-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="23b15-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="23b15-154">DefaultLineStyle Property</span></span>  <br/> |<span data-ttu-id="23b15-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23b15-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23b15-156">opcional</span><span class="sxs-lookup"><span data-stu-id="23b15-156">optional</span></span>  <br/> ||<span data-ttu-id="23b15-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="23b15-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="23b15-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="23b15-158">expression  . DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="23b15-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23b15-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23b15-160">opcional</span><span class="sxs-lookup"><span data-stu-id="23b15-160">optional</span></span>  <br/> ||<span data-ttu-id="23b15-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="23b15-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="23b15-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="23b15-162">TopPage</span></span>  <br/> |<span data-ttu-id="23b15-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23b15-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23b15-164">opcional</span><span class="sxs-lookup"><span data-stu-id="23b15-164">optional</span></span>  <br/> ||<span data-ttu-id="23b15-165">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="23b15-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

