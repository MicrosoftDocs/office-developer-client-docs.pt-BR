---
title: Window_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773285"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="a2e56-102">Window_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a2e56-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a2e56-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="a2e56-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2e56-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2e56-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a2e56-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a2e56-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a2e56-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a2e56-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a2e56-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="a2e56-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a2e56-108">None</span><span class="sxs-lookup"><span data-stu-id="a2e56-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2e56-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a2e56-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a2e56-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a2e56-110">Elements and attributes</span></span>

<span data-ttu-id="a2e56-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a2e56-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2e56-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a2e56-112">Child elements</span></span>

|<span data-ttu-id="a2e56-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a2e56-113">**Element**</span></span>|<span data-ttu-id="a2e56-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2e56-114">**Type**</span></span>|<span data-ttu-id="a2e56-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2e56-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a2e56-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="a2e56-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="a2e56-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="a2e56-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="a2e56-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="a2e56-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="a2e56-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="a2e56-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="a2e56-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="a2e56-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="a2e56-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="a2e56-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="a2e56-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2e56-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="a2e56-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2e56-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="a2e56-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a2e56-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2e56-142">Attributes</span></span>

|<span data-ttu-id="a2e56-143">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a2e56-143">**Attribute**</span></span>|<span data-ttu-id="a2e56-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2e56-144">**Type**</span></span>|<span data-ttu-id="a2e56-145">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a2e56-145">**Required**</span></span>|<span data-ttu-id="a2e56-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2e56-146">**Description**</span></span>|<span data-ttu-id="a2e56-147">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a2e56-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2e56-148">Container</span><span class="sxs-lookup"><span data-stu-id="a2e56-148">Container</span></span>  <br/> |<span data-ttu-id="a2e56-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-150">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-150">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="a2e56-152">ContainerType</span></span>  <br/> |<span data-ttu-id="a2e56-153">XSD:token</span><span class="sxs-lookup"><span data-stu-id="a2e56-153">xsd:token</span></span>  <br/> |<span data-ttu-id="a2e56-154">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-154">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-155">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a2e56-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-156">Document</span><span class="sxs-lookup"><span data-stu-id="a2e56-156">Document</span></span>  <br/> |<span data-ttu-id="a2e56-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a2e56-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a2e56-158">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-158">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-159">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a2e56-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-160">Id</span><span class="sxs-lookup"><span data-stu-id="a2e56-160">ID</span></span>  <br/> |<span data-ttu-id="a2e56-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2e56-162">required</span></span>  <br/> ||<span data-ttu-id="a2e56-163">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-164">Master</span><span class="sxs-lookup"><span data-stu-id="a2e56-164">Master</span></span>  <br/> |<span data-ttu-id="a2e56-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-166">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-166">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-168">Page</span><span class="sxs-lookup"><span data-stu-id="a2e56-168">Page</span></span>  <br/> |<span data-ttu-id="a2e56-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-170">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-170">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-171">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="a2e56-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="a2e56-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-174">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-174">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-175">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a2e56-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="a2e56-177">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e56-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2e56-178">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-178">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-179">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a2e56-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-180">Planilha</span><span class="sxs-lookup"><span data-stu-id="a2e56-180">Sheet</span></span>  <br/> |<span data-ttu-id="a2e56-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-182">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-182">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-183">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="a2e56-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="a2e56-185">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a2e56-185">xsd:double</span></span>  <br/> |<span data-ttu-id="a2e56-186">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-186">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-187">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a2e56-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="a2e56-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="a2e56-189">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a2e56-189">xsd:double</span></span>  <br/> |<span data-ttu-id="a2e56-190">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-190">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-191">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a2e56-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="a2e56-192">ViewScale</span></span>  <br/> |<span data-ttu-id="a2e56-193">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="a2e56-193">xsd:double</span></span>  <br/> |<span data-ttu-id="a2e56-194">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-194">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-195">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="a2e56-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="a2e56-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="a2e56-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-198">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-198">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-199">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="a2e56-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="a2e56-201">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="a2e56-201">xsd:short</span></span>  <br/> |<span data-ttu-id="a2e56-202">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-202">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-203">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="a2e56-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="a2e56-204">WindowState</span></span>  <br/> |<span data-ttu-id="a2e56-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-206">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-206">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-207">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="a2e56-208">WindowTop</span></span>  <br/> |<span data-ttu-id="a2e56-209">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="a2e56-209">xsd:short</span></span>  <br/> |<span data-ttu-id="a2e56-210">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-210">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-211">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="a2e56-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="a2e56-212">WindowType</span></span>  <br/> |<span data-ttu-id="a2e56-213">XSD:token</span><span class="sxs-lookup"><span data-stu-id="a2e56-213">xsd:token</span></span>  <br/> |<span data-ttu-id="a2e56-214">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2e56-214">required</span></span>  <br/> ||<span data-ttu-id="a2e56-215">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a2e56-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a2e56-216">LarguraDaJanela</span><span class="sxs-lookup"><span data-stu-id="a2e56-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="a2e56-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2e56-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2e56-218">opcional</span><span class="sxs-lookup"><span data-stu-id="a2e56-218">optional</span></span>  <br/> ||<span data-ttu-id="a2e56-219">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2e56-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

