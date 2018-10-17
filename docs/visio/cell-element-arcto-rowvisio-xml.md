---
title: Elemento Cell (Linha ArcTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Contém a coordenada x, a coordenada y ou a curva de um arco circular.
ms.openlocfilehash: 709251c40299425d59df97fc0c48901bb0204167
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393058"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="4a195-103">Elemento Cell (Linha ArcTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4a195-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="4a195-104">Contém a coordenada x, a coordenada y ou a curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="4a195-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a195-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="4a195-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a195-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4a195-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4a195-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4a195-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4a195-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4a195-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4a195-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4a195-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4a195-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4a195-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4a195-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="4a195-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4a195-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="4a195-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a195-113">Definição</span><span class="sxs-lookup"><span data-stu-id="4a195-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a195-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4a195-114">Elements and attributes</span></span>

<span data-ttu-id="4a195-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4a195-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4a195-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4a195-116">Parent elements</span></span>

|<span data-ttu-id="4a195-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a195-117">**Element**</span></span>|<span data-ttu-id="4a195-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a195-118">**Type**</span></span>|<span data-ttu-id="4a195-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a195-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a195-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="4a195-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4a195-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="4a195-121">ArcTo_Type complexType</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a195-122">Contém as coordenadas x e y ou a curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="4a195-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4a195-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4a195-123">Child elements</span></span>

|<span data-ttu-id="4a195-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a195-124">**Element**</span></span>|<span data-ttu-id="4a195-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a195-125">**Type**</span></span>|<span data-ttu-id="4a195-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a195-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a195-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="4a195-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a195-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4a195-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a195-129">Contém a coordenada x, a coordenada y ou a curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="4a195-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4a195-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a195-130">Attributes</span></span>

|<span data-ttu-id="4a195-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4a195-131">**Attribute**</span></span>|<span data-ttu-id="4a195-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a195-132">**Type**</span></span>|<span data-ttu-id="4a195-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4a195-133">**Required**</span></span>|<span data-ttu-id="4a195-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a195-134">**Description**</span></span>|<span data-ttu-id="4a195-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4a195-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a195-136">E</span><span class="sxs-lookup"><span data-stu-id="4a195-136">E</span></span>  <br/> |<span data-ttu-id="4a195-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a195-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4a195-138">opcional</span><span class="sxs-lookup"><span data-stu-id="4a195-138">optional</span></span>  <br/> |<span data-ttu-id="4a195-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="4a195-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="4a195-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="4a195-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="4a195-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="4a195-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="4a195-142">F</span><span class="sxs-lookup"><span data-stu-id="4a195-142">F</span></span>  <br/> |<span data-ttu-id="4a195-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a195-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4a195-144">opcional</span><span class="sxs-lookup"><span data-stu-id="4a195-144">optional</span></span>  <br/> | <span data-ttu-id="4a195-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="4a195-145">Represents the element's formula.</span></span> <span data-ttu-id="4a195-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="4a195-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="4a195-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="4a195-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="4a195-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="4a195-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="4a195-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="4a195-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="4a195-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="4a195-150">A formula</span></span>  <br/> |
|<span data-ttu-id="4a195-151">N</span><span class="sxs-lookup"><span data-stu-id="4a195-151">N</span></span>  <br/> |<span data-ttu-id="4a195-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a195-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4a195-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4a195-153">required</span></span>  <br/> |<span data-ttu-id="4a195-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4a195-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="4a195-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4a195-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="4a195-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="4a195-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="4a195-157">S</span><span class="sxs-lookup"><span data-stu-id="4a195-157">U</span></span>  <br/> |<span data-ttu-id="4a195-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a195-158">xsd:string</span></span>  <br/> |<span data-ttu-id="4a195-159">opcional</span><span class="sxs-lookup"><span data-stu-id="4a195-159">optional</span></span>  <br/> |<span data-ttu-id="4a195-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="4a195-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="4a195-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="4a195-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="4a195-162">S</span><span class="sxs-lookup"><span data-stu-id="4a195-162">v</span></span>  <br/> |<span data-ttu-id="4a195-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a195-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4a195-164">opcional</span><span class="sxs-lookup"><span data-stu-id="4a195-164">optional</span></span>  <br/> |<span data-ttu-id="4a195-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="4a195-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="4a195-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4a195-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a195-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a195-167">Remarks</span></span>

<span data-ttu-id="4a195-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4a195-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="4a195-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="4a195-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="4a195-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4a195-170">**Value**</span></span>|<span data-ttu-id="4a195-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a195-171">**Description**</span></span>|<span data-ttu-id="4a195-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="4a195-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a195-173">A</span><span class="sxs-lookup"><span data-stu-id="4a195-173">A</span></span>  <br/> |<span data-ttu-id="4a195-174">A distância entre o ponto médio do arco e o ponto médio da corda dele.</span><span class="sxs-lookup"><span data-stu-id="4a195-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="4a195-175">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="4a195-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="4a195-176">X</span><span class="sxs-lookup"><span data-stu-id="4a195-176">x</span></span>  <br/> |<span data-ttu-id="4a195-177">A coordenada x do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="4a195-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="4a195-178">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="4a195-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="4a195-179">S</span><span class="sxs-lookup"><span data-stu-id="4a195-179">Y</span></span>  <br/> |<span data-ttu-id="4a195-180">A coordenada y do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="4a195-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="4a195-181">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="4a195-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

