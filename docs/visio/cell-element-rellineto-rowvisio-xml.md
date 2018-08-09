---
title: Elemento de célula (RelLineTo linha) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: Contém x- ou coordenadas y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.
ms.openlocfilehash: 73930b15a62a483b38da4791511f735ac81bb1a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771481"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="6f459-103">Elemento de célula (RelLineTo linha) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6f459-103">Cell element (RelLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="6f459-104">Contém x- ou coordenadas y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6f459-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f459-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="6f459-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f459-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6f459-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6f459-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6f459-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6f459-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6f459-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6f459-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6f459-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6f459-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6f459-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6f459-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6f459-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6f459-112"># XML do mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="6f459-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f459-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6f459-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6f459-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6f459-114">Elements and attributes</span></span>

<span data-ttu-id="6f459-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6f459-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6f459-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6f459-116">Parent elements</span></span>

|<span data-ttu-id="6f459-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f459-117">**Element**</span></span>|<span data-ttu-id="6f459-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f459-118">**Type**</span></span>|<span data-ttu-id="6f459-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f459-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f459-120">Elemento de linha (Geometry)</span><span class="sxs-lookup"><span data-stu-id="6f459-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6f459-121">RelLineTo_Type</span><span class="sxs-lookup"><span data-stu-id="6f459-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6f459-122">Contém x- ou coordenadas y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6f459-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6f459-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6f459-123">Child elements</span></span>

|<span data-ttu-id="6f459-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f459-124">**Element**</span></span>|<span data-ttu-id="6f459-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f459-125">**Type**</span></span>|<span data-ttu-id="6f459-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f459-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f459-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="6f459-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f459-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="6f459-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6f459-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="6f459-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6f459-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f459-130">Attributes</span></span>

|<span data-ttu-id="6f459-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6f459-131">**Attribute**</span></span>|<span data-ttu-id="6f459-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f459-132">**Type**</span></span>|<span data-ttu-id="6f459-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6f459-133">**Required**</span></span>|<span data-ttu-id="6f459-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f459-134">**Description**</span></span>|<span data-ttu-id="6f459-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6f459-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6f459-136">E</span><span class="sxs-lookup"><span data-stu-id="6f459-136">E</span></span>  <br/> |<span data-ttu-id="6f459-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6f459-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6f459-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6f459-138">optional</span></span>  <br/> |<span data-ttu-id="6f459-139">Indica que a fórmula é avaliada como um erro.</span><span class="sxs-lookup"><span data-stu-id="6f459-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="6f459-140">O valor de **f** é o valor atual (uma sequência de mensagem de erro;) o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="6f459-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="6f459-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6f459-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="6f459-142">S</span><span class="sxs-lookup"><span data-stu-id="6f459-142">F</span></span>  <br/> |<span data-ttu-id="6f459-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6f459-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6f459-144">opcional</span><span class="sxs-lookup"><span data-stu-id="6f459-144">optional</span></span>  <br/> | <span data-ttu-id="6f459-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="6f459-145">Represents the element's formula.</span></span> <span data-ttu-id="6f459-146">Este atributo pode conter uma das cadeias de caracteres seguintes:</span><span class="sxs-lookup"><span data-stu-id="6f459-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="6f459-147">'(alguns formula)' se a fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="6f459-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="6f459-148">`No Formula`Se a fórmula localmente é excluída ou bloqueada</span><span class="sxs-lookup"><span data-stu-id="6f459-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="6f459-149">`Inh`Se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="6f459-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="6f459-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="6f459-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="6f459-151">N</span><span class="sxs-lookup"><span data-stu-id="6f459-151">N</span></span>  <br/> |<span data-ttu-id="6f459-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6f459-152">xsd:string</span></span>  <br/> |<span data-ttu-id="6f459-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6f459-153">required</span></span>  <br/> |<span data-ttu-id="6f459-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6f459-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="6f459-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6f459-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="6f459-156">Consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="6f459-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="6f459-157">U</span><span class="sxs-lookup"><span data-stu-id="6f459-157">U</span></span>  <br/> |<span data-ttu-id="6f459-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6f459-158">xsd:string</span></span>  <br/> |<span data-ttu-id="6f459-159">opcional</span><span class="sxs-lookup"><span data-stu-id="6f459-159">optional</span></span>  <br/> |<span data-ttu-id="6f459-160">Representa uma unidade de medida padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="6f459-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="6f459-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="6f459-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="6f459-162">V</span><span class="sxs-lookup"><span data-stu-id="6f459-162">V</span></span>  <br/> |<span data-ttu-id="6f459-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6f459-163">xsd:string</span></span>  <br/> |<span data-ttu-id="6f459-164">opcional</span><span class="sxs-lookup"><span data-stu-id="6f459-164">optional</span></span>  <br/> |<span data-ttu-id="6f459-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="6f459-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="6f459-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6f459-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f459-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f459-167">Remarks</span></span>

<span data-ttu-id="6f459-168">O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6f459-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="6f459-169">Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** .</span><span class="sxs-lookup"><span data-stu-id="6f459-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="6f459-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f459-170">**Value**</span></span>|<span data-ttu-id="6f459-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f459-171">**Description**</span></span>|<span data-ttu-id="6f459-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="6f459-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f459-173">X</span><span class="sxs-lookup"><span data-stu-id="6f459-173">X</span></span>  <br/> |<span data-ttu-id="6f459-174">A coordenada x do vértice final de um segmento de linha reta em relação à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="6f459-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |[<span data-ttu-id="6f459-175">Linha RelLineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="6f459-175">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="6f459-176">Y</span><span class="sxs-lookup"><span data-stu-id="6f459-176">Y</span></span>  <br/> |<span data-ttu-id="6f459-177">A coordenada y do vértice final de um segmento de linha reta em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="6f459-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |[<span data-ttu-id="6f459-178">Linha RelLineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="6f459-178">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
   

