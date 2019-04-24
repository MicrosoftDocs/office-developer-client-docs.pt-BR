---
title: Elemento Cell (Seção Tabs) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: Especifica uma propriedade que controla a posição ou o alinhamento da parada de tabulação da forma ou do estilo.
ms.openlocfilehash: c6641c452144544dc769616130c96d6cf89aca23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339638"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="fbebe-103">Elemento Cell (Seção Tabs) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fbebe-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="fbebe-104">Especifica uma propriedade que controla a posição ou o alinhamento da parada de tabulação da forma ou do estilo.</span><span class="sxs-lookup"><span data-stu-id="fbebe-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fbebe-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="fbebe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbebe-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fbebe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fbebe-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fbebe-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fbebe-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fbebe-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fbebe-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fbebe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fbebe-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fbebe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fbebe-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="fbebe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fbebe-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="fbebe-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbebe-113">Definição</span><span class="sxs-lookup"><span data-stu-id="fbebe-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbebe-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fbebe-114">Elements and attributes</span></span>

<span data-ttu-id="fbebe-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fbebe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbebe-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fbebe-116">Parent elements</span></span>

|<span data-ttu-id="fbebe-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbebe-117">**Element**</span></span>|<span data-ttu-id="fbebe-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbebe-118">**Type**</span></span>|<span data-ttu-id="fbebe-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbebe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbebe-120">Elemento Row (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="fbebe-120">Row element (Tabs Section)</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fbebe-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="fbebe-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbebe-122">Especifica uma propriedade que controla a posição ou o alinhamento da parada de tabulação da forma ou do estilo.</span><span class="sxs-lookup"><span data-stu-id="fbebe-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbebe-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fbebe-123">Child elements</span></span>

|<span data-ttu-id="fbebe-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbebe-124">**Element**</span></span>|<span data-ttu-id="fbebe-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbebe-125">**Type**</span></span>|<span data-ttu-id="fbebe-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbebe-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbebe-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="fbebe-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fbebe-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="fbebe-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbebe-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="fbebe-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fbebe-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbebe-130">Attributes</span></span>

|<span data-ttu-id="fbebe-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fbebe-131">**Attribute**</span></span>|<span data-ttu-id="fbebe-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbebe-132">**Type**</span></span>|<span data-ttu-id="fbebe-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fbebe-133">**Required**</span></span>|<span data-ttu-id="fbebe-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbebe-134">**Description**</span></span>|<span data-ttu-id="fbebe-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fbebe-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fbebe-136">E</span><span class="sxs-lookup"><span data-stu-id="fbebe-136">E</span></span>  <br/> |<span data-ttu-id="fbebe-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fbebe-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fbebe-138">opcional</span><span class="sxs-lookup"><span data-stu-id="fbebe-138">optional</span></span>  <br/> |<span data-ttu-id="fbebe-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="fbebe-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="fbebe-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="fbebe-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="fbebe-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="fbebe-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="fbebe-142">F</span><span class="sxs-lookup"><span data-stu-id="fbebe-142">F</span></span>  <br/> |<span data-ttu-id="fbebe-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fbebe-143">xsd:string</span></span>  <br/> |<span data-ttu-id="fbebe-144">opcional</span><span class="sxs-lookup"><span data-stu-id="fbebe-144">optional</span></span>  <br/> | <span data-ttu-id="fbebe-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="fbebe-145">Represents the element's formula.</span></span> <span data-ttu-id="fbebe-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="fbebe-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="fbebe-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="fbebe-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="fbebe-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="fbebe-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="fbebe-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="fbebe-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="fbebe-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="fbebe-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="fbebe-151">N</span><span class="sxs-lookup"><span data-stu-id="fbebe-151">N</span></span>  <br/> |<span data-ttu-id="fbebe-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fbebe-152">xsd:string</span></span>  <br/> |<span data-ttu-id="fbebe-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbebe-153">required</span></span>  <br/> |<span data-ttu-id="fbebe-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fbebe-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="fbebe-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fbebe-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="fbebe-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="fbebe-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="fbebe-157">U</span><span class="sxs-lookup"><span data-stu-id="fbebe-157">U</span></span>  <br/> |<span data-ttu-id="fbebe-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fbebe-158">xsd:string</span></span>  <br/> |<span data-ttu-id="fbebe-159">opcional</span><span class="sxs-lookup"><span data-stu-id="fbebe-159">optional</span></span>  <br/> |<span data-ttu-id="fbebe-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="fbebe-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="fbebe-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="fbebe-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="fbebe-162">S</span><span class="sxs-lookup"><span data-stu-id="fbebe-162">V</span></span>  <br/> |<span data-ttu-id="fbebe-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fbebe-163">xsd:string</span></span>  <br/> |<span data-ttu-id="fbebe-164">opcional</span><span class="sxs-lookup"><span data-stu-id="fbebe-164">optional</span></span>  <br/> |<span data-ttu-id="fbebe-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="fbebe-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="fbebe-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fbebe-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbebe-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbebe-167">Remarks</span></span>

<span data-ttu-id="fbebe-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fbebe-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="fbebe-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="fbebe-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="fbebe-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fbebe-170">**Value**</span></span>|<span data-ttu-id="fbebe-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbebe-171">**Description**</span></span>|<span data-ttu-id="fbebe-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="fbebe-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbebe-173">Alinhamento</span><span class="sxs-lookup"><span data-stu-id="fbebe-173">Alignment</span></span>  <br/> |<span data-ttu-id="fbebe-174">Especifica o alinhamento da guia.</span><span class="sxs-lookup"><span data-stu-id="fbebe-174">Specifies the tab alignment.</span></span>  <br/> |[<span data-ttu-id="fbebe-175">Célula Alignment (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="fbebe-175">Alignment Cell (Tabs Section)</span></span>](alignment-cell-tabs-section.md) <br/> |
|<span data-ttu-id="fbebe-176">Posição</span><span class="sxs-lookup"><span data-stu-id="fbebe-176">Position</span></span>  <br/> |<span data-ttu-id="fbebe-p104">Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.</span><span class="sxs-lookup"><span data-stu-id="fbebe-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |[<span data-ttu-id="fbebe-180">Célula Position (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="fbebe-180">Position Cell (Tabs Section)</span></span>](position-cell-tabs-section.md) <br/> |
   

