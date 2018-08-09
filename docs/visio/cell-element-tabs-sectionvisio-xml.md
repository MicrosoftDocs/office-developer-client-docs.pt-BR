---
title: Elemento de célula (seção Tabs) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: Especifica uma propriedade que controla o alinhamento ou forma e estilo de parada de tabulação.
ms.openlocfilehash: da2fb31688227180bb38a4366c3293a2e16600c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771474"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="95c79-103">Elemento de célula (seção Tabs) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="95c79-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="95c79-104">Especifica uma propriedade que controla o alinhamento ou forma e estilo de parada de tabulação.</span><span class="sxs-lookup"><span data-stu-id="95c79-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="95c79-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="95c79-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95c79-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="95c79-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95c79-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="95c79-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95c79-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95c79-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95c79-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="95c79-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95c79-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="95c79-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95c79-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="95c79-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95c79-112">Document,. XML de n º de mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="95c79-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95c79-113">Definição</span><span class="sxs-lookup"><span data-stu-id="95c79-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95c79-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="95c79-114">Elements and attributes</span></span>

<span data-ttu-id="95c79-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="95c79-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95c79-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="95c79-116">Parent elements</span></span>

|<span data-ttu-id="95c79-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95c79-117">**Element**</span></span>|<span data-ttu-id="95c79-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95c79-118">**Type**</span></span>|<span data-ttu-id="95c79-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95c79-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95c79-120">Elemento Row (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="95c79-120">Row element (Tabs Section)</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="95c79-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="95c79-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95c79-122">Especifica uma propriedade que controla o alinhamento ou forma e estilo de parada de tabulação.</span><span class="sxs-lookup"><span data-stu-id="95c79-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95c79-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="95c79-123">Child elements</span></span>

|<span data-ttu-id="95c79-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95c79-124">**Element**</span></span>|<span data-ttu-id="95c79-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95c79-125">**Type**</span></span>|<span data-ttu-id="95c79-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95c79-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95c79-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="95c79-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95c79-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="95c79-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95c79-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="95c79-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95c79-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="95c79-130">Attributes</span></span>

|<span data-ttu-id="95c79-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="95c79-131">**Attribute**</span></span>|<span data-ttu-id="95c79-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95c79-132">**Type**</span></span>|<span data-ttu-id="95c79-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="95c79-133">**Required**</span></span>|<span data-ttu-id="95c79-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95c79-134">**Description**</span></span>|<span data-ttu-id="95c79-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="95c79-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95c79-136">E</span><span class="sxs-lookup"><span data-stu-id="95c79-136">E</span></span>  <br/> |<span data-ttu-id="95c79-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="95c79-137">xsd:string</span></span>  <br/> |<span data-ttu-id="95c79-138">opcional</span><span class="sxs-lookup"><span data-stu-id="95c79-138">optional</span></span>  <br/> |<span data-ttu-id="95c79-139">Indica que a fórmula é avaliada como um erro.</span><span class="sxs-lookup"><span data-stu-id="95c79-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="95c79-140">O valor de **f** é o valor atual (uma sequência de mensagem de erro;) o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="95c79-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="95c79-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="95c79-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="95c79-142">S</span><span class="sxs-lookup"><span data-stu-id="95c79-142">F</span></span>  <br/> |<span data-ttu-id="95c79-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="95c79-143">xsd:string</span></span>  <br/> |<span data-ttu-id="95c79-144">opcional</span><span class="sxs-lookup"><span data-stu-id="95c79-144">optional</span></span>  <br/> | <span data-ttu-id="95c79-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="95c79-145">Represents the element's formula.</span></span> <span data-ttu-id="95c79-146">Este atributo pode conter uma das cadeias de caracteres seguintes:</span><span class="sxs-lookup"><span data-stu-id="95c79-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="95c79-147">'(alguns formula)' se a fórmula existe localmente</span><span class="sxs-lookup"><span data-stu-id="95c79-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="95c79-148">`No Formula`Se a fórmula localmente é excluída ou bloqueada</span><span class="sxs-lookup"><span data-stu-id="95c79-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="95c79-149">`Inh`Se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="95c79-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="95c79-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="95c79-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="95c79-151">N</span><span class="sxs-lookup"><span data-stu-id="95c79-151">N</span></span>  <br/> |<span data-ttu-id="95c79-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="95c79-152">xsd:string</span></span>  <br/> |<span data-ttu-id="95c79-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="95c79-153">required</span></span>  <br/> |<span data-ttu-id="95c79-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="95c79-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="95c79-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="95c79-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="95c79-156">Consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="95c79-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="95c79-157">U</span><span class="sxs-lookup"><span data-stu-id="95c79-157">U</span></span>  <br/> |<span data-ttu-id="95c79-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="95c79-158">xsd:string</span></span>  <br/> |<span data-ttu-id="95c79-159">opcional</span><span class="sxs-lookup"><span data-stu-id="95c79-159">optional</span></span>  <br/> |<span data-ttu-id="95c79-160">Representa uma unidade de medida padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="95c79-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="95c79-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="95c79-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="95c79-162">V</span><span class="sxs-lookup"><span data-stu-id="95c79-162">V</span></span>  <br/> |<span data-ttu-id="95c79-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="95c79-163">xsd:string</span></span>  <br/> |<span data-ttu-id="95c79-164">opcional</span><span class="sxs-lookup"><span data-stu-id="95c79-164">optional</span></span>  <br/> |<span data-ttu-id="95c79-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="95c79-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="95c79-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="95c79-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95c79-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c79-167">Remarks</span></span>

<span data-ttu-id="95c79-168">O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="95c79-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="95c79-169">Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** .</span><span class="sxs-lookup"><span data-stu-id="95c79-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="95c79-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="95c79-170">**Value**</span></span>|<span data-ttu-id="95c79-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95c79-171">**Description**</span></span>|<span data-ttu-id="95c79-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="95c79-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95c79-173">Alinhamento</span><span class="sxs-lookup"><span data-stu-id="95c79-173">Alignment</span></span>  <br/> |<span data-ttu-id="95c79-174">Especifica o alinhamento de tabulação.</span><span class="sxs-lookup"><span data-stu-id="95c79-174">Specifies the tab alignment.</span></span>  <br/> |[<span data-ttu-id="95c79-175">Célula Alignment (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="95c79-175">Alignment Cell (Tabs Section)</span></span>](alignment-cell-tabs-section.md) <br/> |
|<span data-ttu-id="95c79-176">Position</span><span class="sxs-lookup"><span data-stu-id="95c79-176">Position</span></span>  <br/> |<span data-ttu-id="95c79-p104">Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.</span><span class="sxs-lookup"><span data-stu-id="95c79-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |[<span data-ttu-id="95c79-180">Célula Position (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="95c79-180">Position Cell (Tabs Section)</span></span>](position-cell-tabs-section.md) <br/> |
   

