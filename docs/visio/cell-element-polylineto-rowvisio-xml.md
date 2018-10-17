---
title: Elemento Cell (Linha PolyLineTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Contém as coordenadas x ou y do último ponto de uma polilinha ou uma fórmula de polilinha.
ms.openlocfilehash: 7a27cc5a4c2b6c9833263a28bbcadc40f08d8e70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398651"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="46efa-103">Elemento Cell (Linha PolyLineTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="46efa-103">Cell element (PolyLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="46efa-104">Contém as coordenadas x ou y do último ponto de uma polilinha ou uma fórmula de polilinha.</span><span class="sxs-lookup"><span data-stu-id="46efa-104">Contains x- and y-coordinates of the last point of a polyline and a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46efa-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="46efa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46efa-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="46efa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="46efa-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="46efa-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="46efa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="46efa-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="46efa-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="46efa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="46efa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="46efa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="46efa-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="46efa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="46efa-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="46efa-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46efa-113">Definição</span><span class="sxs-lookup"><span data-stu-id="46efa-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46efa-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="46efa-114">Elements and attributes</span></span>

<span data-ttu-id="46efa-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="46efa-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="46efa-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="46efa-116">Parent elements</span></span>

|<span data-ttu-id="46efa-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46efa-117">**Element**</span></span>|<span data-ttu-id="46efa-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="46efa-118">**Type**</span></span>|<span data-ttu-id="46efa-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46efa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46efa-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="46efa-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="46efa-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="46efa-121">PolylineTo_Type complexType</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46efa-122">Contém as coordenadas x ou y do último ponto de uma polilinha ou uma fórmula de polilinha.</span><span class="sxs-lookup"><span data-stu-id="46efa-122">Contains x- and y-coordinates of the last point of a polyline and a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="46efa-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="46efa-123">Child elements</span></span>

|<span data-ttu-id="46efa-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46efa-124">**Element**</span></span>|<span data-ttu-id="46efa-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="46efa-125">**Type**</span></span>|<span data-ttu-id="46efa-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46efa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46efa-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="46efa-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46efa-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="46efa-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46efa-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="46efa-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="46efa-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="46efa-130">Attributes</span></span>

|<span data-ttu-id="46efa-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="46efa-131">**Attribute**</span></span>|<span data-ttu-id="46efa-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="46efa-132">**Type**</span></span>|<span data-ttu-id="46efa-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="46efa-133">**Required**</span></span>|<span data-ttu-id="46efa-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46efa-134">**Description**</span></span>|<span data-ttu-id="46efa-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="46efa-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="46efa-136">E</span><span class="sxs-lookup"><span data-stu-id="46efa-136">E</span></span>  <br/> |<span data-ttu-id="46efa-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="46efa-137">xsd:string</span></span>  <br/> |<span data-ttu-id="46efa-138">opcional</span><span class="sxs-lookup"><span data-stu-id="46efa-138">optional</span></span>  <br/> |<span data-ttu-id="46efa-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="46efa-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="46efa-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="46efa-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="46efa-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="46efa-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="46efa-142">F</span><span class="sxs-lookup"><span data-stu-id="46efa-142">F</span></span>  <br/> |<span data-ttu-id="46efa-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="46efa-143">xsd:string</span></span>  <br/> |<span data-ttu-id="46efa-144">opcional</span><span class="sxs-lookup"><span data-stu-id="46efa-144">optional</span></span>  <br/> | <span data-ttu-id="46efa-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="46efa-145">Represents the element's formula.</span></span> <span data-ttu-id="46efa-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="46efa-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="46efa-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="46efa-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="46efa-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="46efa-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="46efa-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="46efa-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="46efa-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="46efa-150">A formula</span></span>  <br/> |
|<span data-ttu-id="46efa-151">N</span><span class="sxs-lookup"><span data-stu-id="46efa-151">N</span></span>  <br/> |<span data-ttu-id="46efa-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="46efa-152">xsd:string</span></span>  <br/> |<span data-ttu-id="46efa-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="46efa-153">required</span></span>  <br/> |<span data-ttu-id="46efa-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="46efa-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="46efa-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="46efa-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="46efa-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="46efa-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="46efa-157">S</span><span class="sxs-lookup"><span data-stu-id="46efa-157">U</span></span>  <br/> |<span data-ttu-id="46efa-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="46efa-158">xsd:string</span></span>  <br/> |<span data-ttu-id="46efa-159">opcional</span><span class="sxs-lookup"><span data-stu-id="46efa-159">optional</span></span>  <br/> |<span data-ttu-id="46efa-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="46efa-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="46efa-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="46efa-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="46efa-162">S</span><span class="sxs-lookup"><span data-stu-id="46efa-162">v</span></span>  <br/> |<span data-ttu-id="46efa-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="46efa-163">xsd:string</span></span>  <br/> |<span data-ttu-id="46efa-164">opcional</span><span class="sxs-lookup"><span data-stu-id="46efa-164">optional</span></span>  <br/> |<span data-ttu-id="46efa-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="46efa-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="46efa-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="46efa-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46efa-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="46efa-167">Remarks</span></span>

<span data-ttu-id="46efa-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="46efa-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="46efa-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="46efa-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="46efa-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="46efa-170">**Value**</span></span>|<span data-ttu-id="46efa-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46efa-171">**Description**</span></span>|<span data-ttu-id="46efa-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="46efa-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46efa-173">X</span><span class="sxs-lookup"><span data-stu-id="46efa-173">x</span></span>  <br/> |<span data-ttu-id="46efa-174">A coordenada x do vértice final de uma linha múltipla.</span><span class="sxs-lookup"><span data-stu-id="46efa-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="46efa-175">Linha PolylineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="46efa-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="46efa-176">S</span><span class="sxs-lookup"><span data-stu-id="46efa-176">Y</span></span>  <br/> |<span data-ttu-id="46efa-177">A coordenada y do vértice final de uma linha múltipla.</span><span class="sxs-lookup"><span data-stu-id="46efa-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="46efa-178">Linha PolylineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="46efa-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="46efa-179">A</span><span class="sxs-lookup"><span data-stu-id="46efa-179">A</span></span>  <br/> |<span data-ttu-id="46efa-180">A fórmula da linha múltipla.</span><span class="sxs-lookup"><span data-stu-id="46efa-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="46efa-181">Linha PolylineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="46efa-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

