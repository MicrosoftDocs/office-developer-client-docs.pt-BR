---
title: Elemento Cell (Linha SplineKnot) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.
ms.openlocfilehash: 1f2ddbcf7b750f2c2de983e16861070c7305fc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339785"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="26411-103">Elemento Cell (Linha SplineKnot) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="26411-103">Cell element (SplineKnot Row) ('Visio XML')</span></span>

<span data-ttu-id="26411-104">Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="26411-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26411-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="26411-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26411-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="26411-106">**Element type**</span></span> <br/> |[<span data-ttu-id="26411-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="26411-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="26411-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26411-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="26411-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="26411-109">**Schema file**</span></span> <br/> |<span data-ttu-id="26411-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="26411-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="26411-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="26411-111">**Document parts**</span></span> <br/> |<span data-ttu-id="26411-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="26411-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26411-113">Definição</span><span class="sxs-lookup"><span data-stu-id="26411-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26411-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="26411-114">Elements and attributes</span></span>

<span data-ttu-id="26411-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="26411-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="26411-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="26411-116">Parent elements</span></span>

|<span data-ttu-id="26411-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26411-117">**Element**</span></span>|<span data-ttu-id="26411-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26411-118">**Type**</span></span>|<span data-ttu-id="26411-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26411-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26411-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="26411-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="26411-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="26411-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26411-122">Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="26411-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26411-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="26411-123">Child elements</span></span>

|<span data-ttu-id="26411-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26411-124">**Element**</span></span>|<span data-ttu-id="26411-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26411-125">**Type**</span></span>|<span data-ttu-id="26411-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26411-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26411-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="26411-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26411-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="26411-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26411-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="26411-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="26411-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="26411-130">Attributes</span></span>

|<span data-ttu-id="26411-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="26411-131">**Attribute**</span></span>|<span data-ttu-id="26411-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26411-132">**Type**</span></span>|<span data-ttu-id="26411-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="26411-133">**Required**</span></span>|<span data-ttu-id="26411-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26411-134">**Description**</span></span>|<span data-ttu-id="26411-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="26411-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26411-136">E</span><span class="sxs-lookup"><span data-stu-id="26411-136">E</span></span>  <br/> |<span data-ttu-id="26411-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26411-137">xsd:string</span></span>  <br/> |<span data-ttu-id="26411-138">opcional</span><span class="sxs-lookup"><span data-stu-id="26411-138">optional</span></span>  <br/> |<span data-ttu-id="26411-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="26411-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="26411-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="26411-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="26411-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="26411-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="26411-142">F</span><span class="sxs-lookup"><span data-stu-id="26411-142">F</span></span>  <br/> |<span data-ttu-id="26411-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26411-143">xsd:string</span></span>  <br/> |<span data-ttu-id="26411-144">opcional</span><span class="sxs-lookup"><span data-stu-id="26411-144">optional</span></span>  <br/> | <span data-ttu-id="26411-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="26411-145">Represents the element's formula.</span></span> <span data-ttu-id="26411-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="26411-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="26411-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="26411-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="26411-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="26411-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="26411-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="26411-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="26411-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="26411-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="26411-151">N</span><span class="sxs-lookup"><span data-stu-id="26411-151">N</span></span>  <br/> |<span data-ttu-id="26411-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26411-152">xsd:string</span></span>  <br/> |<span data-ttu-id="26411-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="26411-153">required</span></span>  <br/> |<span data-ttu-id="26411-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="26411-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="26411-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="26411-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="26411-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="26411-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="26411-157">U</span><span class="sxs-lookup"><span data-stu-id="26411-157">U</span></span>  <br/> |<span data-ttu-id="26411-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26411-158">xsd:string</span></span>  <br/> |<span data-ttu-id="26411-159">opcional</span><span class="sxs-lookup"><span data-stu-id="26411-159">optional</span></span>  <br/> |<span data-ttu-id="26411-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="26411-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="26411-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="26411-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="26411-162">S</span><span class="sxs-lookup"><span data-stu-id="26411-162">V</span></span>  <br/> |<span data-ttu-id="26411-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26411-163">xsd:string</span></span>  <br/> |<span data-ttu-id="26411-164">opcional</span><span class="sxs-lookup"><span data-stu-id="26411-164">optional</span></span>  <br/> |<span data-ttu-id="26411-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="26411-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="26411-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="26411-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26411-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="26411-167">Remarks</span></span>

<span data-ttu-id="26411-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="26411-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="26411-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="26411-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="26411-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26411-170">**Value**</span></span>|<span data-ttu-id="26411-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26411-171">**Description**</span></span>|<span data-ttu-id="26411-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="26411-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26411-173">X</span><span class="sxs-lookup"><span data-stu-id="26411-173">X</span></span>  <br/> |<span data-ttu-id="26411-174">A coordenada x do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="26411-174">The x-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="26411-175">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="26411-175">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="26411-176">S</span><span class="sxs-lookup"><span data-stu-id="26411-176">Y</span></span>  <br/> |<span data-ttu-id="26411-177">A coordenada y do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="26411-177">The y-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="26411-178">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="26411-178">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="26411-179">A</span><span class="sxs-lookup"><span data-stu-id="26411-179">A</span></span>  <br/> |<span data-ttu-id="26411-180">Um dos nós da spline (sem ser o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="26411-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |[<span data-ttu-id="26411-181">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="26411-181">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
   

