---
title: Elemento Cell (Linha LineTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contém as coordenadas x ou y do vértice final de um segmento de linha reta.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386590"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="efeee-103">Elemento Cell (Linha LineTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="efeee-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="efeee-104">Contém as coordenadas x ou y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="efeee-104">Contains x-and y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efeee-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="efeee-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efeee-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="efeee-106">**Element type**</span></span> <br/> |[<span data-ttu-id="efeee-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="efeee-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="efeee-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="efeee-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="efeee-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="efeee-109">**Schema file**</span></span> <br/> |<span data-ttu-id="efeee-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="efeee-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="efeee-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="efeee-111">**Document parts**</span></span> <br/> |<span data-ttu-id="efeee-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="efeee-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efeee-113">Definição</span><span class="sxs-lookup"><span data-stu-id="efeee-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="efeee-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="efeee-114">Elements and attributes</span></span>

<span data-ttu-id="efeee-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="efeee-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="efeee-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="efeee-116">Parent elements</span></span>

|<span data-ttu-id="efeee-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="efeee-117">**Element**</span></span>|<span data-ttu-id="efeee-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efeee-118">**Type**</span></span>|<span data-ttu-id="efeee-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="efeee-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efeee-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="efeee-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="efeee-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="efeee-121">LineTo_Type complexType</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="efeee-122">Contém as coordenadas x ou y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="efeee-122">Contains x-and y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="efeee-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="efeee-123">Child elements</span></span>

|<span data-ttu-id="efeee-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="efeee-124">**Element**</span></span>|<span data-ttu-id="efeee-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efeee-125">**Type**</span></span>|<span data-ttu-id="efeee-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="efeee-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efeee-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="efeee-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efeee-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="efeee-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="efeee-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="efeee-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="efeee-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="efeee-130">Attributes</span></span>

|<span data-ttu-id="efeee-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="efeee-131">**Attribute**</span></span>|<span data-ttu-id="efeee-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efeee-132">**Type**</span></span>|<span data-ttu-id="efeee-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="efeee-133">**Required**</span></span>|<span data-ttu-id="efeee-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="efeee-134">**Description**</span></span>|<span data-ttu-id="efeee-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="efeee-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efeee-136">E</span><span class="sxs-lookup"><span data-stu-id="efeee-136">E</span></span>  <br/> |<span data-ttu-id="efeee-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="efeee-137">xsd:string</span></span>  <br/> |<span data-ttu-id="efeee-138">opcional</span><span class="sxs-lookup"><span data-stu-id="efeee-138">optional</span></span>  <br/> |<span data-ttu-id="efeee-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="efeee-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="efeee-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="efeee-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="efeee-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="efeee-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="efeee-142">F</span><span class="sxs-lookup"><span data-stu-id="efeee-142">F</span></span>  <br/> |<span data-ttu-id="efeee-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="efeee-143">xsd:string</span></span>  <br/> |<span data-ttu-id="efeee-144">opcional</span><span class="sxs-lookup"><span data-stu-id="efeee-144">optional</span></span>  <br/> | <span data-ttu-id="efeee-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="efeee-145">Represents the element's formula.</span></span> <span data-ttu-id="efeee-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="efeee-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="efeee-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="efeee-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="efeee-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="efeee-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="efeee-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="efeee-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="efeee-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="efeee-150">A formula</span></span>  <br/> |
|<span data-ttu-id="efeee-151">N</span><span class="sxs-lookup"><span data-stu-id="efeee-151">N</span></span>  <br/> |<span data-ttu-id="efeee-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="efeee-152">xsd:string</span></span>  <br/> |<span data-ttu-id="efeee-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="efeee-153">required</span></span>  <br/> |<span data-ttu-id="efeee-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="efeee-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="efeee-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="efeee-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="efeee-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="efeee-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="efeee-157">S</span><span class="sxs-lookup"><span data-stu-id="efeee-157">U</span></span>  <br/> |<span data-ttu-id="efeee-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="efeee-158">xsd:string</span></span>  <br/> |<span data-ttu-id="efeee-159">opcional</span><span class="sxs-lookup"><span data-stu-id="efeee-159">optional</span></span>  <br/> |<span data-ttu-id="efeee-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="efeee-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="efeee-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="efeee-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="efeee-162">S</span><span class="sxs-lookup"><span data-stu-id="efeee-162">v</span></span>  <br/> |<span data-ttu-id="efeee-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="efeee-163">xsd:string</span></span>  <br/> |<span data-ttu-id="efeee-164">opcional</span><span class="sxs-lookup"><span data-stu-id="efeee-164">optional</span></span>  <br/> |<span data-ttu-id="efeee-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="efeee-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="efeee-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="efeee-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efeee-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="efeee-167">Remarks</span></span>

<span data-ttu-id="efeee-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="efeee-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="efeee-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="efeee-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="efeee-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="efeee-170">**Value**</span></span>|<span data-ttu-id="efeee-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="efeee-171">**Description**</span></span>|<span data-ttu-id="efeee-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="efeee-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="efeee-173">X</span><span class="sxs-lookup"><span data-stu-id="efeee-173">x</span></span>  <br/> |<span data-ttu-id="efeee-174">A coordenada x do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="efeee-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="efeee-175">Linha LineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="efeee-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="efeee-176">S</span><span class="sxs-lookup"><span data-stu-id="efeee-176">Y</span></span>  <br/> |<span data-ttu-id="efeee-177">A coordenada y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="efeee-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="efeee-178">Linha LineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="efeee-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

