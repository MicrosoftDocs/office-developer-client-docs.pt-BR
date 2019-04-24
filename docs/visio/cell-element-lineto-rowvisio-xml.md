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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318197"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="8e9f6-103">Elemento Cell (Linha LineTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8e9f6-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="8e9f6-104">Contém as coordenadas x ou y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e9f6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="8e9f6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e9f6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8e9f6-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8e9f6-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8e9f6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8e9f6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8e9f6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8e9f6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8e9f6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8e9f6-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="8e9f6-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e9f6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8e9f6-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8e9f6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8e9f6-114">Elements and attributes</span></span>

<span data-ttu-id="8e9f6-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8e9f6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8e9f6-116">Parent elements</span></span>

|<span data-ttu-id="8e9f6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-117">**Element**</span></span>|<span data-ttu-id="8e9f6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-118">**Type**</span></span>|<span data-ttu-id="8e9f6-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e9f6-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="8e9f6-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8e9f6-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="8e9f6-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e9f6-122">Contém as coordenadas x ou y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e9f6-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8e9f6-123">Child elements</span></span>

|<span data-ttu-id="8e9f6-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-124">**Element**</span></span>|<span data-ttu-id="8e9f6-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-125">**Type**</span></span>|<span data-ttu-id="8e9f6-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e9f6-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="8e9f6-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8e9f6-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="8e9f6-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e9f6-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8e9f6-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e9f6-130">Attributes</span></span>

|<span data-ttu-id="8e9f6-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-131">**Attribute**</span></span>|<span data-ttu-id="8e9f6-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-132">**Type**</span></span>|<span data-ttu-id="8e9f6-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-133">**Required**</span></span>|<span data-ttu-id="8e9f6-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-134">**Description**</span></span>|<span data-ttu-id="8e9f6-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8e9f6-136">E</span><span class="sxs-lookup"><span data-stu-id="8e9f6-136">E</span></span>  <br/> |<span data-ttu-id="8e9f6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e9f6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8e9f6-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8e9f6-138">optional</span></span>  <br/> |<span data-ttu-id="8e9f6-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="8e9f6-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="8e9f6-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="8e9f6-142">F</span><span class="sxs-lookup"><span data-stu-id="8e9f6-142">F</span></span>  <br/> |<span data-ttu-id="8e9f6-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e9f6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8e9f6-144">opcional</span><span class="sxs-lookup"><span data-stu-id="8e9f6-144">optional</span></span>  <br/> | <span data-ttu-id="8e9f6-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-145">Represents the element's formula.</span></span> <span data-ttu-id="8e9f6-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="8e9f6-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="8e9f6-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="8e9f6-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="8e9f6-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="8e9f6-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="8e9f6-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="8e9f6-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="8e9f6-151">N</span><span class="sxs-lookup"><span data-stu-id="8e9f6-151">N</span></span>  <br/> |<span data-ttu-id="8e9f6-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e9f6-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8e9f6-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8e9f6-153">required</span></span>  <br/> |<span data-ttu-id="8e9f6-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="8e9f6-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="8e9f6-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="8e9f6-157">U</span><span class="sxs-lookup"><span data-stu-id="8e9f6-157">U</span></span>  <br/> |<span data-ttu-id="8e9f6-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e9f6-158">xsd:string</span></span>  <br/> |<span data-ttu-id="8e9f6-159">opcional</span><span class="sxs-lookup"><span data-stu-id="8e9f6-159">optional</span></span>  <br/> |<span data-ttu-id="8e9f6-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="8e9f6-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="8e9f6-162">S</span><span class="sxs-lookup"><span data-stu-id="8e9f6-162">V</span></span>  <br/> |<span data-ttu-id="8e9f6-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8e9f6-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8e9f6-164">opcional</span><span class="sxs-lookup"><span data-stu-id="8e9f6-164">optional</span></span>  <br/> |<span data-ttu-id="8e9f6-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="8e9f6-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e9f6-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e9f6-167">Remarks</span></span>

<span data-ttu-id="8e9f6-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="8e9f6-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="8e9f6-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-170">**Value**</span></span>|<span data-ttu-id="8e9f6-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-171">**Description**</span></span>|<span data-ttu-id="8e9f6-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="8e9f6-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e9f6-173">X</span><span class="sxs-lookup"><span data-stu-id="8e9f6-173">X</span></span>  <br/> |<span data-ttu-id="8e9f6-174">A coordenada x do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="8e9f6-175">Linha LineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="8e9f6-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="8e9f6-176">S</span><span class="sxs-lookup"><span data-stu-id="8e9f6-176">Y</span></span>  <br/> |<span data-ttu-id="8e9f6-177">A coordenada y do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="8e9f6-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="8e9f6-178">Linha LineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="8e9f6-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

