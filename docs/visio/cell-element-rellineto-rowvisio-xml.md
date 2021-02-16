---
title: Elemento Cell (Linha RelLineTo) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: Contém as coordenadas x ou y do vértice final de um segmento de linha reta relativa à largura e altura da forma.
ms.openlocfilehash: 1a3277eac2b0f759d3da6cb93b5339f97a5ac876
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539415"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="96e58-103">Elemento Cell (Linha RelLineTo) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="96e58-103">Cell element (RelLineTo Row) (Visio XML)</span></span>

<span data-ttu-id="96e58-104">Contém as coordenadas x ou y do vértice final de um segmento de linha reta relativa à largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="96e58-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96e58-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="96e58-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96e58-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="96e58-106">**Element type**</span></span> <br/> |[<span data-ttu-id="96e58-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="96e58-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="96e58-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="96e58-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="96e58-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="96e58-109">**Schema file**</span></span> <br/> |<span data-ttu-id="96e58-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="96e58-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="96e58-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="96e58-111">**Document parts**</span></span> <br/> |<span data-ttu-id="96e58-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="96e58-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96e58-113">Definição</span><span class="sxs-lookup"><span data-stu-id="96e58-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="96e58-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="96e58-114">Elements and attributes</span></span>

<span data-ttu-id="96e58-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="96e58-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="96e58-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="96e58-116">Parent elements</span></span>

|<span data-ttu-id="96e58-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96e58-117">**Element**</span></span>|<span data-ttu-id="96e58-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="96e58-118">**Type**</span></span>|<span data-ttu-id="96e58-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96e58-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96e58-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="96e58-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="96e58-121">RelLineTo_Type</span><span class="sxs-lookup"><span data-stu-id="96e58-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96e58-122">Contém as coordenadas x ou y do vértice final de um segmento de linha reta relativa à largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="96e58-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="96e58-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="96e58-123">Child elements</span></span>

|<span data-ttu-id="96e58-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96e58-124">**Element**</span></span>|<span data-ttu-id="96e58-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="96e58-125">**Type**</span></span>|<span data-ttu-id="96e58-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96e58-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96e58-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="96e58-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96e58-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="96e58-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96e58-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="96e58-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="96e58-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="96e58-130">Attributes</span></span>

|<span data-ttu-id="96e58-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="96e58-131">**Attribute**</span></span>|<span data-ttu-id="96e58-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="96e58-132">**Type**</span></span>|<span data-ttu-id="96e58-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="96e58-133">**Required**</span></span>|<span data-ttu-id="96e58-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96e58-134">**Description**</span></span>|<span data-ttu-id="96e58-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="96e58-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96e58-136">E</span><span class="sxs-lookup"><span data-stu-id="96e58-136">E</span></span>  <br/> |<span data-ttu-id="96e58-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="96e58-137">xsd:string</span></span>  <br/> |<span data-ttu-id="96e58-138">opcional</span><span class="sxs-lookup"><span data-stu-id="96e58-138">optional</span></span>  <br/> |<span data-ttu-id="96e58-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="96e58-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="96e58-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="96e58-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="96e58-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="96e58-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="96e58-142">F</span><span class="sxs-lookup"><span data-stu-id="96e58-142">F</span></span>  <br/> |<span data-ttu-id="96e58-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="96e58-143">xsd:string</span></span>  <br/> |<span data-ttu-id="96e58-144">opcional</span><span class="sxs-lookup"><span data-stu-id="96e58-144">optional</span></span>  <br/> | <span data-ttu-id="96e58-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="96e58-145">Represents the element's formula.</span></span> <span data-ttu-id="96e58-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="96e58-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="96e58-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="96e58-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="96e58-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="96e58-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="96e58-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="96e58-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="96e58-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="96e58-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="96e58-151">N</span><span class="sxs-lookup"><span data-stu-id="96e58-151">N</span></span>  <br/> |<span data-ttu-id="96e58-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="96e58-152">xsd:string</span></span>  <br/> |<span data-ttu-id="96e58-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="96e58-153">required</span></span>  <br/> |<span data-ttu-id="96e58-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="96e58-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="96e58-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="96e58-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="96e58-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="96e58-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="96e58-157">U</span><span class="sxs-lookup"><span data-stu-id="96e58-157">U</span></span>  <br/> |<span data-ttu-id="96e58-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="96e58-158">xsd:string</span></span>  <br/> |<span data-ttu-id="96e58-159">opcional</span><span class="sxs-lookup"><span data-stu-id="96e58-159">optional</span></span>  <br/> |<span data-ttu-id="96e58-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="96e58-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="96e58-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="96e58-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="96e58-162">S</span><span class="sxs-lookup"><span data-stu-id="96e58-162">V</span></span>  <br/> |<span data-ttu-id="96e58-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="96e58-163">xsd:string</span></span>  <br/> |<span data-ttu-id="96e58-164">opcional</span><span class="sxs-lookup"><span data-stu-id="96e58-164">optional</span></span>  <br/> |<span data-ttu-id="96e58-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="96e58-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="96e58-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="96e58-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96e58-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="96e58-167">Remarks</span></span>

<span data-ttu-id="96e58-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="96e58-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="96e58-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="96e58-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="96e58-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="96e58-170">**Value**</span></span>|<span data-ttu-id="96e58-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96e58-171">**Description**</span></span>|<span data-ttu-id="96e58-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="96e58-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96e58-173">X</span><span class="sxs-lookup"><span data-stu-id="96e58-173">X</span></span>  <br/> |<span data-ttu-id="96e58-174">A coordenada x do vértice final de um segmento de linha reta relativa à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="96e58-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |[<span data-ttu-id="96e58-175">Linha RelLineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="96e58-175">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="96e58-176">S</span><span class="sxs-lookup"><span data-stu-id="96e58-176">Y</span></span>  <br/> |<span data-ttu-id="96e58-177">A coordenada x do vértice final de um segmento de linha reta relativa à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="96e58-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |[<span data-ttu-id="96e58-178">Linha RelLineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="96e58-178">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
   

