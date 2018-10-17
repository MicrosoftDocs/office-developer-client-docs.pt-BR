---
title: Elemento Cell (Seção Line Gradient) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: Contém a cor, a transparência ou a posição de uma marca de gradiente para um gradiente de linha.
ms.openlocfilehash: 915341b41849aae2af2285b49f0421798a16cf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392190"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a><span data-ttu-id="c8d0e-103">Elemento Cell (Seção Line Gradient) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c8d0e-103">Cell element (Line Gradient Section)</span></span>

<span data-ttu-id="c8d0e-104">Contém a cor, a transparência ou a posição de uma marca de gradiente para um gradiente de linha.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-104">Contains the color, transparency, or position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8d0e-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c8d0e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8d0e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c8d0e-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c8d0e-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c8d0e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c8d0e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c8d0e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c8d0e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c8d0e-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c8d0e-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c8d0e-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8d0e-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c8d0e-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c8d0e-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c8d0e-114">Elements and attributes</span></span>

<span data-ttu-id="c8d0e-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c8d0e-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c8d0e-116">Parent elements</span></span>

|<span data-ttu-id="c8d0e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-117">**Element**</span></span>|<span data-ttu-id="c8d0e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-118">**Type**</span></span>|<span data-ttu-id="c8d0e-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8d0e-120">Elemento Row (Seção Line Gradient)</span><span class="sxs-lookup"><span data-stu-id="c8d0e-120">Row element (Line Gradient Section)</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c8d0e-121">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="c8d0e-121">LineGradientRow_Type complexType</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c8d0e-122">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8d0e-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c8d0e-123">Child elements</span></span>

|<span data-ttu-id="c8d0e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-124">**Element**</span></span>|<span data-ttu-id="c8d0e-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-125">**Type**</span></span>|<span data-ttu-id="c8d0e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8d0e-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c8d0e-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8d0e-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c8d0e-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c8d0e-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c8d0e-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8d0e-130">Attributes</span></span>

|<span data-ttu-id="c8d0e-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-131">**Attribute**</span></span>|<span data-ttu-id="c8d0e-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-132">**Type**</span></span>|<span data-ttu-id="c8d0e-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-133">**Required**</span></span>|<span data-ttu-id="c8d0e-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-134">**Description**</span></span>|<span data-ttu-id="c8d0e-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c8d0e-136">E</span><span class="sxs-lookup"><span data-stu-id="c8d0e-136">E</span></span>  <br/> |<span data-ttu-id="c8d0e-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8d0e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c8d0e-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c8d0e-138">optional</span></span>  <br/> |<span data-ttu-id="c8d0e-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c8d0e-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c8d0e-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c8d0e-142">F</span><span class="sxs-lookup"><span data-stu-id="c8d0e-142">F</span></span>  <br/> |<span data-ttu-id="c8d0e-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8d0e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c8d0e-144">opcional</span><span class="sxs-lookup"><span data-stu-id="c8d0e-144">optional</span></span>  <br/> | <span data-ttu-id="c8d0e-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-145">Represents the element's formula.</span></span> <span data-ttu-id="c8d0e-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="c8d0e-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c8d0e-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="c8d0e-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c8d0e-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="c8d0e-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c8d0e-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c8d0e-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-150">A formula</span></span>  <br/> |
|<span data-ttu-id="c8d0e-151">N</span><span class="sxs-lookup"><span data-stu-id="c8d0e-151">N</span></span>  <br/> |<span data-ttu-id="c8d0e-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8d0e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c8d0e-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c8d0e-153">required</span></span>  <br/> |<span data-ttu-id="c8d0e-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c8d0e-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c8d0e-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c8d0e-157">S</span><span class="sxs-lookup"><span data-stu-id="c8d0e-157">U</span></span>  <br/> |<span data-ttu-id="c8d0e-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8d0e-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c8d0e-159">opcional</span><span class="sxs-lookup"><span data-stu-id="c8d0e-159">optional</span></span>  <br/> |<span data-ttu-id="c8d0e-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c8d0e-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c8d0e-162">S</span><span class="sxs-lookup"><span data-stu-id="c8d0e-162">v</span></span>  <br/> |<span data-ttu-id="c8d0e-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8d0e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c8d0e-164">opcional</span><span class="sxs-lookup"><span data-stu-id="c8d0e-164">optional</span></span>  <br/> |<span data-ttu-id="c8d0e-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c8d0e-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8d0e-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8d0e-167">Remarks</span></span>

<span data-ttu-id="c8d0e-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c8d0e-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c8d0e-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-170">**Value**</span></span>|<span data-ttu-id="c8d0e-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-171">**Description**</span></span>|<span data-ttu-id="c8d0e-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="c8d0e-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8d0e-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="c8d0e-173">GradientStopColor Property</span></span>  <br/> |<span data-ttu-id="c8d0e-174">O valor de cor da marca de gradiente.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-174">The color value of the gradient stop.</span></span>  <br/> |[<span data-ttu-id="c8d0e-175">Linha Gradient Stop (Seção Line Gradient)</span><span class="sxs-lookup"><span data-stu-id="c8d0e-175">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
|<span data-ttu-id="c8d0e-176">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="c8d0e-176">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="c8d0e-177">A quantidade de transparência da cor da marca de gradiente, em porcentagem.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-177">The amount of transparency of the gradient stop color, as a percentage.</span></span>  <br/> |[<span data-ttu-id="c8d0e-178">Linha Gradient Stop (Seção Line Gradient)</span><span class="sxs-lookup"><span data-stu-id="c8d0e-178">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
|<span data-ttu-id="c8d0e-179">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="c8d0e-179">GradientStopPosition Property</span></span>  <br/> |<span data-ttu-id="c8d0e-180">A posição da marca de gradiente na direção da linha de gradiente, em porcentagem, do ponto de origem do gradiente até a borda externa do gradiente.</span><span class="sxs-lookup"><span data-stu-id="c8d0e-180">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |[<span data-ttu-id="c8d0e-181">Linha Gradient Stop (Seção Line Gradient)</span><span class="sxs-lookup"><span data-stu-id="c8d0e-181">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
   

