---
title: Window_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 340326213de4029201d21e627ed4b27c53b33d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339925"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="b7b43-102">Window_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b7b43-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b7b43-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="b7b43-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7b43-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b7b43-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b7b43-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b7b43-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b7b43-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b7b43-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b7b43-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="b7b43-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b7b43-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7b43-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7b43-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b7b43-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b7b43-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b7b43-110">Elements and attributes</span></span>

<span data-ttu-id="b7b43-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b7b43-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b7b43-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b7b43-112">Child elements</span></span>

|<span data-ttu-id="b7b43-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7b43-113">**Element**</span></span>|<span data-ttu-id="b7b43-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7b43-114">**Type**</span></span>|<span data-ttu-id="b7b43-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b7b43-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7b43-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="b7b43-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="b7b43-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-120">Todos os ConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="b7b43-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="b7b43-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="b7b43-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="b7b43-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="b7b43-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="b7b43-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="b7b43-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="b7b43-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-136">Painel de estêncil</span><span class="sxs-lookup"><span data-stu-id="b7b43-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="b7b43-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b7b43-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="b7b43-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7b43-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="b7b43-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b7b43-142">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7b43-142">Attributes</span></span>

|<span data-ttu-id="b7b43-143">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b7b43-143">**Attribute**</span></span>|<span data-ttu-id="b7b43-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7b43-144">**Type**</span></span>|<span data-ttu-id="b7b43-145">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b7b43-145">**Required**</span></span>|<span data-ttu-id="b7b43-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b7b43-146">**Description**</span></span>|<span data-ttu-id="b7b43-147">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b7b43-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b7b43-148">Contêiner</span><span class="sxs-lookup"><span data-stu-id="b7b43-148">Container</span></span>  <br/> |<span data-ttu-id="b7b43-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-150">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="b7b43-152">ContainerType</span></span>  <br/> |<span data-ttu-id="b7b43-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="b7b43-153">xsd:token</span></span>  <br/> |<span data-ttu-id="b7b43-154">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-154">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-155">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="b7b43-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-156">Documento</span><span class="sxs-lookup"><span data-stu-id="b7b43-156">Document</span></span>  <br/> |<span data-ttu-id="b7b43-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b7b43-157">xsd:string</span></span>  <br/> |<span data-ttu-id="b7b43-158">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-158">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-159">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b7b43-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-160">ID</span><span class="sxs-lookup"><span data-stu-id="b7b43-160">ID</span></span>  <br/> |<span data-ttu-id="b7b43-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b7b43-162">required</span></span>  <br/> ||<span data-ttu-id="b7b43-163">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-164">Mestre</span><span class="sxs-lookup"><span data-stu-id="b7b43-164">Master</span></span>  <br/> |<span data-ttu-id="b7b43-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-166">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-166">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-168">Page</span><span class="sxs-lookup"><span data-stu-id="b7b43-168">Page</span></span>  <br/> |<span data-ttu-id="b7b43-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-170">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-170">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-171">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="b7b43-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="b7b43-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-174">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-174">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-175">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b7b43-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="b7b43-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b7b43-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b7b43-178">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-178">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-179">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b7b43-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-180">Planilha</span><span class="sxs-lookup"><span data-stu-id="b7b43-180">Sheet</span></span>  <br/> |<span data-ttu-id="b7b43-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-182">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-182">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-183">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="b7b43-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="b7b43-185">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="b7b43-185">xsd:double</span></span>  <br/> |<span data-ttu-id="b7b43-186">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-186">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-187">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="b7b43-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="b7b43-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="b7b43-189">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="b7b43-189">xsd:double</span></span>  <br/> |<span data-ttu-id="b7b43-190">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-190">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-191">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="b7b43-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="b7b43-192">ViewScale</span></span>  <br/> |<span data-ttu-id="b7b43-193">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="b7b43-193">xsd:double</span></span>  <br/> |<span data-ttu-id="b7b43-194">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-194">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-195">Valores do tipo xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="b7b43-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="b7b43-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="b7b43-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-198">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-198">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-199">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="b7b43-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="b7b43-201">xsd: Short</span><span class="sxs-lookup"><span data-stu-id="b7b43-201">xsd:short</span></span>  <br/> |<span data-ttu-id="b7b43-202">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-202">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-203">Valores do tipo xsd: short.</span><span class="sxs-lookup"><span data-stu-id="b7b43-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="b7b43-204">WindowState</span></span>  <br/> |<span data-ttu-id="b7b43-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-206">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-206">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-207">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="b7b43-208">WindowTop</span></span>  <br/> |<span data-ttu-id="b7b43-209">xsd: Short</span><span class="sxs-lookup"><span data-stu-id="b7b43-209">xsd:short</span></span>  <br/> |<span data-ttu-id="b7b43-210">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-210">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-211">Valores do tipo xsd: short.</span><span class="sxs-lookup"><span data-stu-id="b7b43-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-212">Windowtype</span><span class="sxs-lookup"><span data-stu-id="b7b43-212">WindowType</span></span>  <br/> |<span data-ttu-id="b7b43-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="b7b43-213">xsd:token</span></span>  <br/> |<span data-ttu-id="b7b43-214">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b7b43-214">required</span></span>  <br/> ||<span data-ttu-id="b7b43-215">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="b7b43-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="b7b43-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="b7b43-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="b7b43-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7b43-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7b43-218">opcional</span><span class="sxs-lookup"><span data-stu-id="b7b43-218">optional</span></span>  <br/> ||<span data-ttu-id="b7b43-219">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7b43-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

