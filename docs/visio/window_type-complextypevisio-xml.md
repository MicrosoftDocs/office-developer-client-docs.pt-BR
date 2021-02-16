---
title: Window_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538449"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="3bce0-102">Window_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3bce0-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3bce0-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3bce0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bce0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3bce0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3bce0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3bce0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3bce0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3bce0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3bce0-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3bce0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3bce0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3bce0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3bce0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3bce0-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
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
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
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
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3bce0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3bce0-110">Elements and attributes</span></span>

<span data-ttu-id="3bce0-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3bce0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3bce0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3bce0-112">Child elements</span></span>

|<span data-ttu-id="3bce0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3bce0-113">**Element**</span></span>|<span data-ttu-id="3bce0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3bce0-114">**Type**</span></span>|<span data-ttu-id="3bce0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3bce0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3bce0-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="3bce0-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="3bce0-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="3bce0-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="3bce0-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="3bce0-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="3bce0-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="3bce0-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="3bce0-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="3bce0-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="3bce0-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="3bce0-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="3bce0-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3bce0-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="3bce0-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bce0-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="3bce0-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3bce0-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="3bce0-142">Attributes</span></span>

|<span data-ttu-id="3bce0-143">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3bce0-143">**Attribute**</span></span>|<span data-ttu-id="3bce0-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3bce0-144">**Type**</span></span>|<span data-ttu-id="3bce0-145">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3bce0-145">**Required**</span></span>|<span data-ttu-id="3bce0-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3bce0-146">**Description**</span></span>|<span data-ttu-id="3bce0-147">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3bce0-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3bce0-148">Contêiner</span><span class="sxs-lookup"><span data-stu-id="3bce0-148">Container</span></span>  <br/> |<span data-ttu-id="3bce0-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-150">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="3bce0-152">ContainerType</span></span>  <br/> |<span data-ttu-id="3bce0-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="3bce0-153">xsd:token</span></span>  <br/> |<span data-ttu-id="3bce0-154">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-154">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-155">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="3bce0-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-156">Document</span><span class="sxs-lookup"><span data-stu-id="3bce0-156">Document</span></span>  <br/> |<span data-ttu-id="3bce0-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3bce0-157">xsd:string</span></span>  <br/> |<span data-ttu-id="3bce0-158">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-158">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-159">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3bce0-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-160">ID</span><span class="sxs-lookup"><span data-stu-id="3bce0-160">ID</span></span>  <br/> |<span data-ttu-id="3bce0-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3bce0-162">required</span></span>  <br/> ||<span data-ttu-id="3bce0-163">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-164">Master</span><span class="sxs-lookup"><span data-stu-id="3bce0-164">Master</span></span>  <br/> |<span data-ttu-id="3bce0-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-166">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-166">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-168">Page</span><span class="sxs-lookup"><span data-stu-id="3bce0-168">Page</span></span>  <br/> |<span data-ttu-id="3bce0-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-170">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-170">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-171">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="3bce0-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="3bce0-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-174">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-174">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-175">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3bce0-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="3bce0-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="3bce0-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3bce0-178">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-178">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-179">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3bce0-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-180">Planilha</span><span class="sxs-lookup"><span data-stu-id="3bce0-180">Sheet</span></span>  <br/> |<span data-ttu-id="3bce0-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-182">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-182">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-183">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="3bce0-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="3bce0-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="3bce0-185">xsd:double</span></span>  <br/> |<span data-ttu-id="3bce0-186">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-186">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-187">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="3bce0-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="3bce0-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="3bce0-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="3bce0-189">xsd:double</span></span>  <br/> |<span data-ttu-id="3bce0-190">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-190">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-191">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="3bce0-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="3bce0-192">ViewScale</span></span>  <br/> |<span data-ttu-id="3bce0-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="3bce0-193">xsd:double</span></span>  <br/> |<span data-ttu-id="3bce0-194">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-194">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-195">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="3bce0-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="3bce0-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="3bce0-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-198">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-198">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-199">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="3bce0-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="3bce0-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="3bce0-201">xsd:short</span></span>  <br/> |<span data-ttu-id="3bce0-202">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-202">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-203">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="3bce0-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="3bce0-204">WindowState</span></span>  <br/> |<span data-ttu-id="3bce0-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-206">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-206">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-207">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="3bce0-208">WindowTop</span></span>  <br/> |<span data-ttu-id="3bce0-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="3bce0-209">xsd:short</span></span>  <br/> |<span data-ttu-id="3bce0-210">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-210">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-211">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="3bce0-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="3bce0-212">WindowType</span></span>  <br/> |<span data-ttu-id="3bce0-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="3bce0-213">xsd:token</span></span>  <br/> |<span data-ttu-id="3bce0-214">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3bce0-214">required</span></span>  <br/> ||<span data-ttu-id="3bce0-215">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="3bce0-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="3bce0-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="3bce0-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="3bce0-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bce0-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bce0-218">opcional</span><span class="sxs-lookup"><span data-stu-id="3bce0-218">optional</span></span>  <br/> ||<span data-ttu-id="3bce0-219">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bce0-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

