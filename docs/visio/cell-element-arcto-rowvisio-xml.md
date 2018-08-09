---
title: Elemento de célula (linha ArcTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Contém o x coordenada coordenada y ou curva de um arco circular.
ms.openlocfilehash: a51cf775f787a34aa8f5de6f6cf90ffc230f3500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771435"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="6e3af-103">Elemento de célula (linha ArcTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6e3af-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="6e3af-104">Contém o x coordenada coordenada y ou curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="6e3af-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e3af-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="6e3af-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e3af-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6e3af-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6e3af-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6e3af-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6e3af-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6e3af-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6e3af-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6e3af-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6e3af-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6e3af-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6e3af-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6e3af-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6e3af-112"># XML do mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="6e3af-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e3af-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6e3af-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e3af-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6e3af-114">Elements and attributes</span></span>

<span data-ttu-id="6e3af-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6e3af-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e3af-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6e3af-116">Parent elements</span></span>

|<span data-ttu-id="6e3af-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e3af-117">**Element**</span></span>|<span data-ttu-id="6e3af-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e3af-118">**Type**</span></span>|<span data-ttu-id="6e3af-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e3af-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e3af-120">Elemento de linha (Geometry)</span><span class="sxs-lookup"><span data-stu-id="6e3af-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6e3af-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="6e3af-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e3af-122">Contém as coordenadas x e y e um arco de uma curva circular.</span><span class="sxs-lookup"><span data-stu-id="6e3af-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e3af-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6e3af-123">Child elements</span></span>

|<span data-ttu-id="6e3af-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e3af-124">**Element**</span></span>|<span data-ttu-id="6e3af-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e3af-125">**Type**</span></span>|<span data-ttu-id="6e3af-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e3af-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e3af-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="6e3af-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e3af-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="6e3af-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e3af-129">Contém o x coordenada coordenada y ou curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="6e3af-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6e3af-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e3af-130">Attributes</span></span>

|<span data-ttu-id="6e3af-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6e3af-131">**Attribute**</span></span>|<span data-ttu-id="6e3af-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e3af-132">**Type**</span></span>|<span data-ttu-id="6e3af-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6e3af-133">**Required**</span></span>|<span data-ttu-id="6e3af-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e3af-134">**Description**</span></span>|<span data-ttu-id="6e3af-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6e3af-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6e3af-136">E</span><span class="sxs-lookup"><span data-stu-id="6e3af-136">E</span></span>  <br/> |<span data-ttu-id="6e3af-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6e3af-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6e3af-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6e3af-138">optional</span></span>  <br/> |<span data-ttu-id="6e3af-139">Indica que a fórmula é avaliada como um erro.</span><span class="sxs-lookup"><span data-stu-id="6e3af-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="6e3af-140">O valor de **f** é o valor atual (uma sequência de mensagem de erro;) o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="6e3af-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="6e3af-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6e3af-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="6e3af-142">S</span><span class="sxs-lookup"><span data-stu-id="6e3af-142">F</span></span>  <br/> |<span data-ttu-id="6e3af-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6e3af-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6e3af-144">opcional</span><span class="sxs-lookup"><span data-stu-id="6e3af-144">optional</span></span>  <br/> | <span data-ttu-id="6e3af-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="6e3af-145">Represents the element's formula.</span></span> <span data-ttu-id="6e3af-146">Este atributo pode conter uma das cadeias de caracteres seguintes:</span><span class="sxs-lookup"><span data-stu-id="6e3af-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="6e3af-147">'(alguns formula)' se a fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="6e3af-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="6e3af-148">`No Formula`Se a fórmula localmente é excluída ou bloqueada</span><span class="sxs-lookup"><span data-stu-id="6e3af-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="6e3af-149">`Inh`Se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="6e3af-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="6e3af-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="6e3af-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="6e3af-151">N</span><span class="sxs-lookup"><span data-stu-id="6e3af-151">N</span></span>  <br/> |<span data-ttu-id="6e3af-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6e3af-152">xsd:string</span></span>  <br/> |<span data-ttu-id="6e3af-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6e3af-153">required</span></span>  <br/> |<span data-ttu-id="6e3af-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6e3af-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="6e3af-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6e3af-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="6e3af-156">Consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="6e3af-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="6e3af-157">U</span><span class="sxs-lookup"><span data-stu-id="6e3af-157">U</span></span>  <br/> |<span data-ttu-id="6e3af-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6e3af-158">xsd:string</span></span>  <br/> |<span data-ttu-id="6e3af-159">opcional</span><span class="sxs-lookup"><span data-stu-id="6e3af-159">optional</span></span>  <br/> |<span data-ttu-id="6e3af-160">Representa uma unidade de medida padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="6e3af-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="6e3af-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="6e3af-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="6e3af-162">V</span><span class="sxs-lookup"><span data-stu-id="6e3af-162">V</span></span>  <br/> |<span data-ttu-id="6e3af-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6e3af-163">xsd:string</span></span>  <br/> |<span data-ttu-id="6e3af-164">opcional</span><span class="sxs-lookup"><span data-stu-id="6e3af-164">optional</span></span>  <br/> |<span data-ttu-id="6e3af-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="6e3af-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="6e3af-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6e3af-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e3af-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e3af-167">Remarks</span></span>

<span data-ttu-id="6e3af-168">O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6e3af-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="6e3af-169">Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** .</span><span class="sxs-lookup"><span data-stu-id="6e3af-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="6e3af-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6e3af-170">**Value**</span></span>|<span data-ttu-id="6e3af-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e3af-171">**Description**</span></span>|<span data-ttu-id="6e3af-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="6e3af-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e3af-173">A</span><span class="sxs-lookup"><span data-stu-id="6e3af-173">A</span></span>  <br/> |<span data-ttu-id="6e3af-174">A distância do ponto médio de um arco até o ponto médio de sua corda.</span><span class="sxs-lookup"><span data-stu-id="6e3af-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="6e3af-175">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="6e3af-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="6e3af-176">X</span><span class="sxs-lookup"><span data-stu-id="6e3af-176">X</span></span>  <br/> |<span data-ttu-id="6e3af-177">A coordenada x de um vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="6e3af-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="6e3af-178">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="6e3af-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="6e3af-179">Y</span><span class="sxs-lookup"><span data-stu-id="6e3af-179">Y</span></span>  <br/> |<span data-ttu-id="6e3af-180">A coordenada y de um vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="6e3af-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="6e3af-181">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="6e3af-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

