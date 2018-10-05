---
title: Window_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 340326213de4029201d21e627ed4b27c53b33d1e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400583"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="ae2be-102">Window_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ae2be-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ae2be-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ae2be-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae2be-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ae2be-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ae2be-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ae2be-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ae2be-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ae2be-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ae2be-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ae2be-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ae2be-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ae2be-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae2be-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ae2be-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ae2be-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ae2be-110">Elements and attributes</span></span>

<span data-ttu-id="ae2be-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ae2be-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ae2be-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ae2be-112">Child elements</span></span>

|<span data-ttu-id="ae2be-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ae2be-113">**Element**</span></span>|<span data-ttu-id="ae2be-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ae2be-114">**Type**</span></span>|<span data-ttu-id="ae2be-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae2be-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae2be-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="ae2be-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="ae2be-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="ae2be-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="ae2be-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="ae2be-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="ae2be-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="ae2be-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="ae2be-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="ae2be-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="ae2be-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="ae2be-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="ae2be-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ae2be-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="ae2be-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae2be-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="ae2be-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ae2be-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae2be-142">Attributes</span></span>

|<span data-ttu-id="ae2be-143">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ae2be-143">**Attribute**</span></span>|<span data-ttu-id="ae2be-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ae2be-144">**Type**</span></span>|<span data-ttu-id="ae2be-145">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ae2be-145">**Required**</span></span>|<span data-ttu-id="ae2be-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae2be-146">**Description**</span></span>|<span data-ttu-id="ae2be-147">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ae2be-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ae2be-148">Container</span><span class="sxs-lookup"><span data-stu-id="ae2be-148">Container</span></span>  <br/> |<span data-ttu-id="ae2be-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-150">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-150">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ae2be-152">ContainerType</span></span>  <br/> |<span data-ttu-id="ae2be-153">XSD:token</span><span class="sxs-lookup"><span data-stu-id="ae2be-153">xsd:token</span></span>  <br/> |<span data-ttu-id="ae2be-154">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-154">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-155">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="ae2be-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-156">Document</span><span class="sxs-lookup"><span data-stu-id="ae2be-156">Document</span></span>  <br/> |<span data-ttu-id="ae2be-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ae2be-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ae2be-158">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-158">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-159">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ae2be-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-160">ID</span><span class="sxs-lookup"><span data-stu-id="ae2be-160">ID</span></span>  <br/> |<span data-ttu-id="ae2be-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae2be-162">required</span></span>  <br/> ||<span data-ttu-id="ae2be-163">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-164">Master</span><span class="sxs-lookup"><span data-stu-id="ae2be-164">Master</span></span>  <br/> |<span data-ttu-id="ae2be-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-166">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-166">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-168">Page</span><span class="sxs-lookup"><span data-stu-id="ae2be-168">Page</span></span>  <br/> |<span data-ttu-id="ae2be-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-170">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-170">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-171">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ae2be-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="ae2be-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-174">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-174">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-175">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ae2be-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="ae2be-177">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ae2be-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ae2be-178">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-178">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-179">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ae2be-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-180">Planilha</span><span class="sxs-lookup"><span data-stu-id="ae2be-180">Sheet</span></span>  <br/> |<span data-ttu-id="ae2be-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-182">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-182">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-183">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="ae2be-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="ae2be-185">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="ae2be-185">xsd:double</span></span>  <br/> |<span data-ttu-id="ae2be-186">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-186">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-187">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ae2be-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="ae2be-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="ae2be-189">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="ae2be-189">xsd:double</span></span>  <br/> |<span data-ttu-id="ae2be-190">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-190">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-191">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ae2be-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="ae2be-192">ViewScale</span></span>  <br/> |<span data-ttu-id="ae2be-193">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="ae2be-193">xsd:double</span></span>  <br/> |<span data-ttu-id="ae2be-194">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-194">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-195">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ae2be-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="ae2be-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="ae2be-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-198">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-198">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-199">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="ae2be-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="ae2be-201">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="ae2be-201">xsd:short</span></span>  <br/> |<span data-ttu-id="ae2be-202">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-202">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-203">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="ae2be-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="ae2be-204">WindowState</span></span>  <br/> |<span data-ttu-id="ae2be-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-206">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-206">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-207">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="ae2be-208">WindowTop</span></span>  <br/> |<span data-ttu-id="ae2be-209">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="ae2be-209">xsd:short</span></span>  <br/> |<span data-ttu-id="ae2be-210">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-210">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-211">Valores do tipo xsd:short.</span><span class="sxs-lookup"><span data-stu-id="ae2be-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="ae2be-212">WindowType</span></span>  <br/> |<span data-ttu-id="ae2be-213">XSD:token</span><span class="sxs-lookup"><span data-stu-id="ae2be-213">xsd:token</span></span>  <br/> |<span data-ttu-id="ae2be-214">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae2be-214">required</span></span>  <br/> ||<span data-ttu-id="ae2be-215">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="ae2be-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ae2be-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="ae2be-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="ae2be-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae2be-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae2be-218">opcional</span><span class="sxs-lookup"><span data-stu-id="ae2be-218">optional</span></span>  <br/> ||<span data-ttu-id="ae2be-219">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae2be-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

