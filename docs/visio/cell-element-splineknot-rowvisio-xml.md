---
title: Elemento Cell (Linha SplineKnot) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.
ms.openlocfilehash: 4eb6e2ce47adae20738c0d210ad2dc30f362200d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539366"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="1744c-103">Elemento Cell (Linha SplineKnot) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1744c-103">Cell element (SplineKnot Row) (Visio XML)</span></span>

<span data-ttu-id="1744c-104">Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="1744c-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1744c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="1744c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1744c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1744c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1744c-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1744c-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1744c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1744c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1744c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1744c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1744c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1744c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1744c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1744c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1744c-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="1744c-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1744c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1744c-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1744c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1744c-114">Elements and attributes</span></span>

<span data-ttu-id="1744c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1744c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1744c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1744c-116">Parent elements</span></span>

|<span data-ttu-id="1744c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1744c-117">**Element**</span></span>|<span data-ttu-id="1744c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1744c-118">**Type**</span></span>|<span data-ttu-id="1744c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1744c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1744c-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="1744c-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1744c-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="1744c-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1744c-122">Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="1744c-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1744c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1744c-123">Child elements</span></span>

|<span data-ttu-id="1744c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1744c-124">**Element**</span></span>|<span data-ttu-id="1744c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1744c-125">**Type**</span></span>|<span data-ttu-id="1744c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1744c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1744c-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="1744c-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1744c-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="1744c-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1744c-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="1744c-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1744c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1744c-130">Attributes</span></span>

|<span data-ttu-id="1744c-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1744c-131">**Attribute**</span></span>|<span data-ttu-id="1744c-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1744c-132">**Type**</span></span>|<span data-ttu-id="1744c-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1744c-133">**Required**</span></span>|<span data-ttu-id="1744c-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1744c-134">**Description**</span></span>|<span data-ttu-id="1744c-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1744c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1744c-136">E</span><span class="sxs-lookup"><span data-stu-id="1744c-136">E</span></span>  <br/> |<span data-ttu-id="1744c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1744c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1744c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1744c-138">optional</span></span>  <br/> |<span data-ttu-id="1744c-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="1744c-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="1744c-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="1744c-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="1744c-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1744c-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="1744c-142">F</span><span class="sxs-lookup"><span data-stu-id="1744c-142">F</span></span>  <br/> |<span data-ttu-id="1744c-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1744c-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1744c-144">opcional</span><span class="sxs-lookup"><span data-stu-id="1744c-144">optional</span></span>  <br/> | <span data-ttu-id="1744c-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="1744c-145">Represents the element's formula.</span></span> <span data-ttu-id="1744c-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="1744c-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="1744c-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="1744c-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="1744c-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="1744c-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="1744c-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="1744c-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="1744c-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="1744c-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="1744c-151">N</span><span class="sxs-lookup"><span data-stu-id="1744c-151">N</span></span>  <br/> |<span data-ttu-id="1744c-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1744c-152">xsd:string</span></span>  <br/> |<span data-ttu-id="1744c-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1744c-153">required</span></span>  <br/> |<span data-ttu-id="1744c-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1744c-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="1744c-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1744c-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="1744c-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="1744c-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="1744c-157">U</span><span class="sxs-lookup"><span data-stu-id="1744c-157">U</span></span>  <br/> |<span data-ttu-id="1744c-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1744c-158">xsd:string</span></span>  <br/> |<span data-ttu-id="1744c-159">opcional</span><span class="sxs-lookup"><span data-stu-id="1744c-159">optional</span></span>  <br/> |<span data-ttu-id="1744c-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="1744c-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="1744c-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="1744c-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="1744c-162">S</span><span class="sxs-lookup"><span data-stu-id="1744c-162">V</span></span>  <br/> |<span data-ttu-id="1744c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1744c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1744c-164">opcional</span><span class="sxs-lookup"><span data-stu-id="1744c-164">optional</span></span>  <br/> |<span data-ttu-id="1744c-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="1744c-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="1744c-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1744c-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1744c-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="1744c-167">Remarks</span></span>

<span data-ttu-id="1744c-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1744c-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="1744c-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="1744c-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="1744c-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1744c-170">**Value**</span></span>|<span data-ttu-id="1744c-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1744c-171">**Description**</span></span>|<span data-ttu-id="1744c-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="1744c-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1744c-173">X</span><span class="sxs-lookup"><span data-stu-id="1744c-173">X</span></span>  <br/> |<span data-ttu-id="1744c-174">A coordenada x do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="1744c-174">The x-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="1744c-175">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="1744c-175">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="1744c-176">S</span><span class="sxs-lookup"><span data-stu-id="1744c-176">Y</span></span>  <br/> |<span data-ttu-id="1744c-177">A coordenada y do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="1744c-177">The y-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="1744c-178">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="1744c-178">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="1744c-179">A</span><span class="sxs-lookup"><span data-stu-id="1744c-179">A</span></span>  <br/> |<span data-ttu-id="1744c-180">Um dos nós da spline (sem ser o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="1744c-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |[<span data-ttu-id="1744c-181">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="1744c-181">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
   

