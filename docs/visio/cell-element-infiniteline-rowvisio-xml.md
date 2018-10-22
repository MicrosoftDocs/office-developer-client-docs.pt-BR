---
title: Elemento Cell (Linha InfiniteLine) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e14b8246-0064-3a54-7bd6-ad28180f9ea6
description: Contém as coordenadas x ou y de dois pontos em uma linha infinita.
ms.openlocfilehash: 1dde7958116824efffce6247855a959fee61e869
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392785"
---
# <a name="cell-element-infiniteline-row-visio-xml"></a><span data-ttu-id="2c3b3-103">Elemento Cell (Linha InfiniteLine) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2c3b3-103">Cell element (InfiniteLine Row) ('Visio XML')</span></span>

<span data-ttu-id="2c3b3-104">Contém as coordenadas x ou y de dois pontos em uma linha infinita.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-104">Contains the x- and y-coordinates of two points on an infinite line.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c3b3-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2c3b3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c3b3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2c3b3-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2c3b3-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2c3b3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2c3b3-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2c3b3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2c3b3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2c3b3-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2c3b3-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="2c3b3-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2c3b3-113">Definição</span><span class="sxs-lookup"><span data-stu-id="2c3b3-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2c3b3-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2c3b3-114">Elements and attributes</span></span>

<span data-ttu-id="2c3b3-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2c3b3-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2c3b3-116">Parent elements</span></span>

|<span data-ttu-id="2c3b3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-117">**Element**</span></span>|<span data-ttu-id="2c3b3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-118">**Type**</span></span>|<span data-ttu-id="2c3b3-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2c3b3-120">Elemento Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="2c3b3-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2c3b3-121">InfiniteLine_Type</span><span class="sxs-lookup"><span data-stu-id="2c3b3-121">InfiniteLine_Type complexType</span></span>](infiniteline_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2c3b3-122">Contém as coordenadas x ou y de dois pontos em uma linha infinita.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-122">Contains the x- and y-coordinates of two points on an infinite line.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c3b3-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2c3b3-123">Child elements</span></span>

|<span data-ttu-id="2c3b3-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-124">**Element**</span></span>|<span data-ttu-id="2c3b3-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-125">**Type**</span></span>|<span data-ttu-id="2c3b3-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2c3b3-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="2c3b3-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2c3b3-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="2c3b3-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2c3b3-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2c3b3-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c3b3-130">Attributes</span></span>

|<span data-ttu-id="2c3b3-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-131">**Attribute**</span></span>|<span data-ttu-id="2c3b3-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-132">**Type**</span></span>|<span data-ttu-id="2c3b3-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-133">**Required**</span></span>|<span data-ttu-id="2c3b3-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-134">**Description**</span></span>|<span data-ttu-id="2c3b3-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2c3b3-136">E</span><span class="sxs-lookup"><span data-stu-id="2c3b3-136">E</span></span>  <br/> |<span data-ttu-id="2c3b3-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c3b3-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2c3b3-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2c3b3-138">optional</span></span>  <br/> |<span data-ttu-id="2c3b3-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="2c3b3-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="2c3b3-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="2c3b3-142">F</span><span class="sxs-lookup"><span data-stu-id="2c3b3-142">F</span></span>  <br/> |<span data-ttu-id="2c3b3-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c3b3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="2c3b3-144">opcional</span><span class="sxs-lookup"><span data-stu-id="2c3b3-144">optional</span></span>  <br/> | <span data-ttu-id="2c3b3-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-145">Represents the element's formula.</span></span> <span data-ttu-id="2c3b3-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="2c3b3-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="2c3b3-147">"(alguma fórmula)" se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="2c3b3-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="2c3b3-148">`No Formula` se a fórmula for excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="2c3b3-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="2c3b3-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="2c3b3-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-150">A formula</span></span>  <br/> |
|<span data-ttu-id="2c3b3-151">N</span><span class="sxs-lookup"><span data-stu-id="2c3b3-151">N</span></span>  <br/> |<span data-ttu-id="2c3b3-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c3b3-152">xsd:string</span></span>  <br/> |<span data-ttu-id="2c3b3-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2c3b3-153">required</span></span>  <br/> |<span data-ttu-id="2c3b3-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="2c3b3-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="2c3b3-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="2c3b3-157">U</span><span class="sxs-lookup"><span data-stu-id="2c3b3-157">U</span></span>  <br/> |<span data-ttu-id="2c3b3-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c3b3-158">xsd:string</span></span>  <br/> |<span data-ttu-id="2c3b3-159">opcional</span><span class="sxs-lookup"><span data-stu-id="2c3b3-159">optional</span></span>  <br/> |<span data-ttu-id="2c3b3-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="2c3b3-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="2c3b3-162">V</span><span class="sxs-lookup"><span data-stu-id="2c3b3-162">v</span></span>  <br/> |<span data-ttu-id="2c3b3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c3b3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="2c3b3-164">opcional</span><span class="sxs-lookup"><span data-stu-id="2c3b3-164">optional</span></span>  <br/> |<span data-ttu-id="2c3b3-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="2c3b3-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c3b3-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c3b3-167">Remarks</span></span>

<span data-ttu-id="2c3b3-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondem às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="2c3b3-169">Confira a tabela a seguir para determinar os valores do atributo **N** permitidos para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="2c3b3-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-170">**Value**</span></span>|<span data-ttu-id="2c3b3-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-171">**Description**</span></span>|<span data-ttu-id="2c3b3-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="2c3b3-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c3b3-173">X</span><span class="sxs-lookup"><span data-stu-id="2c3b3-173">x</span></span>  <br/> |<span data-ttu-id="2c3b3-174">Uma coordenada x de um ponto na linha infinita, juntamente com uma coordenada y representada pela célula Y.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-174">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the Y cell.</span></span>  <br/> |[<span data-ttu-id="2c3b3-175">Linha InfiniteLine (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="2c3b3-175">InfiniteLine Row (Geometry Section)</span></span>](infiniteline-row-geometry-section.md) <br/> |
|<span data-ttu-id="2c3b3-176">Y</span><span class="sxs-lookup"><span data-stu-id="2c3b3-176">Y</span></span>  <br/> |<span data-ttu-id="2c3b3-177">Uma coordenada y de um ponto na linha infinita, juntamente com uma coordenada x representada pela célula X.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-177">A y-coordinate of a point on the infinite line; paired with x-coordinate represented by the X cell.</span></span>  <br/> |[<span data-ttu-id="2c3b3-178">Linha InfiniteLine (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="2c3b3-178">InfiniteLine Row (Geometry Section)</span></span>](infiniteline-row-geometry-section.md) <br/> |
|<span data-ttu-id="2c3b3-179">A</span><span class="sxs-lookup"><span data-stu-id="2c3b3-179">A</span></span>  <br/> |<span data-ttu-id="2c3b3-180">Uma coordenada x de um ponto na linha infinita, juntamente com uma coordenada y representada pela célula B.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-180">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the B cell.</span></span>  <br/> |[<span data-ttu-id="2c3b3-181">Linha InfiniteLine (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="2c3b3-181">InfiniteLine Row (Geometry Section)</span></span>](infiniteline-row-geometry-section.md) <br/> |
|<span data-ttu-id="2c3b3-182">B</span><span class="sxs-lookup"><span data-stu-id="2c3b3-182">B</span></span>  <br/> |<span data-ttu-id="2c3b3-183">Uma coordenada y de um ponto em uma linha infinita, juntamente com uma coordenada x representada pela célula A.</span><span class="sxs-lookup"><span data-stu-id="2c3b3-183">A y-coordinate of a point on an infinite line; paired with x-coordinate represented by the A cell.</span></span>  <br/> |[<span data-ttu-id="2c3b3-184">Linha InfiniteLine (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="2c3b3-184">InfiniteLine Row (Geometry Section)</span></span>](infiniteline-row-geometry-section.md) <br/> |
   

