---
title: Elemento Cell (Seção User-defined Cells) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.
ms.openlocfilehash: 0ce456b624f4a4b12a3f2fdc73f56651ea6985ed
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397496"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="fd598-103">Elemento Cell (Seção User-defined Cells) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fd598-103">Cell element (User-defined Cells Section)</span></span>

<span data-ttu-id="fd598-104">Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="fd598-104">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd598-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="fd598-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd598-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fd598-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fd598-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fd598-107">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fd598-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd598-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fd598-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fd598-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fd598-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fd598-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fd598-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="fd598-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fd598-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="fd598-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd598-113">Definição</span><span class="sxs-lookup"><span data-stu-id="fd598-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fd598-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fd598-114">Elements and attributes</span></span>

<span data-ttu-id="fd598-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fd598-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fd598-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fd598-116">Parent elements</span></span>

|<span data-ttu-id="fd598-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fd598-117">**Element**</span></span>|<span data-ttu-id="fd598-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd598-118">**Type**</span></span>|<span data-ttu-id="fd598-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd598-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd598-120">Elemento Row (Seção User-defined Cells)</span><span class="sxs-lookup"><span data-stu-id="fd598-120">Row element (User-defined Cells Section)</span></span>](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fd598-121">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="fd598-121">UserRow_Type complexType</span></span>](userrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fd598-122">Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="fd598-122">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fd598-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fd598-123">Child elements</span></span>

|<span data-ttu-id="fd598-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fd598-124">**Element**</span></span>|<span data-ttu-id="fd598-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd598-125">**Type**</span></span>|<span data-ttu-id="fd598-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd598-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd598-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="fd598-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fd598-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="fd598-128">RefBy_Type complexType</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fd598-129">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="fd598-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fd598-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd598-130">Attributes</span></span>

|<span data-ttu-id="fd598-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fd598-131">**Attribute**</span></span>|<span data-ttu-id="fd598-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd598-132">**Type**</span></span>|<span data-ttu-id="fd598-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fd598-133">**Required**</span></span>|<span data-ttu-id="fd598-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd598-134">**Description**</span></span>|<span data-ttu-id="fd598-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fd598-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd598-136">E</span><span class="sxs-lookup"><span data-stu-id="fd598-136">E</span></span>  <br/> |<span data-ttu-id="fd598-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd598-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fd598-138">opcional</span><span class="sxs-lookup"><span data-stu-id="fd598-138">optional</span></span>  <br/> |<span data-ttu-id="fd598-139">Indica que a fórmula gera um erro.</span><span class="sxs-lookup"><span data-stu-id="fd598-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="fd598-140">O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="fd598-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="fd598-141">Uma cadeia de caracteres de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="fd598-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="fd598-142">F</span><span class="sxs-lookup"><span data-stu-id="fd598-142">F</span></span>  <br/> |<span data-ttu-id="fd598-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd598-143">xsd:string</span></span>  <br/> |<span data-ttu-id="fd598-144">opcional</span><span class="sxs-lookup"><span data-stu-id="fd598-144">optional</span></span>  <br/> | <span data-ttu-id="fd598-145">Representa a fórmula do elemento.</span><span class="sxs-lookup"><span data-stu-id="fd598-145">Represents the element's formula.</span></span> <span data-ttu-id="fd598-146">Esse atributo pode conter uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="fd598-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="fd598-147">'(alguma fórmula)' se a fórmula existir localmente</span><span class="sxs-lookup"><span data-stu-id="fd598-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="fd598-148">`No Formula` se a fórmula estiver excluída ou bloqueada localmente</span><span class="sxs-lookup"><span data-stu-id="fd598-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="fd598-149">`Inh` se a fórmula for herdada.</span><span class="sxs-lookup"><span data-stu-id="fd598-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="fd598-150">Uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="fd598-150">A formula</span></span>  <br/> |
|<span data-ttu-id="fd598-151">N</span><span class="sxs-lookup"><span data-stu-id="fd598-151">N</span></span>  <br/> |<span data-ttu-id="fd598-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd598-152">xsd:string</span></span>  <br/> |<span data-ttu-id="fd598-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="fd598-153">required</span></span>  <br/> |<span data-ttu-id="fd598-154">Representa o nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd598-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="fd598-155">O nome da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd598-155">The name of a ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="fd598-156">Confira a seção Comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="fd598-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="fd598-157">S</span><span class="sxs-lookup"><span data-stu-id="fd598-157">U</span></span>  <br/> |<span data-ttu-id="fd598-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd598-158">xsd:string</span></span>  <br/> |<span data-ttu-id="fd598-159">opcional</span><span class="sxs-lookup"><span data-stu-id="fd598-159">optional</span></span>  <br/> |<span data-ttu-id="fd598-160">Representa uma unidade de medida. O padrão é DL.</span><span class="sxs-lookup"><span data-stu-id="fd598-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="fd598-161">As unidades da célula.</span><span class="sxs-lookup"><span data-stu-id="fd598-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="fd598-162">S</span><span class="sxs-lookup"><span data-stu-id="fd598-162">v</span></span>  <br/> |<span data-ttu-id="fd598-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd598-163">xsd:string</span></span>  <br/> |<span data-ttu-id="fd598-164">opcional</span><span class="sxs-lookup"><span data-stu-id="fd598-164">optional</span></span>  <br/> |<span data-ttu-id="fd598-165">Representa o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="fd598-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="fd598-166">O valor da célula ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd598-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd598-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd598-167">Remarks</span></span>

<span data-ttu-id="fd598-168">O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd598-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="fd598-169">Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="fd598-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="fd598-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd598-170">**Value**</span></span>|<span data-ttu-id="fd598-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd598-171">**Description**</span></span>|<span data-ttu-id="fd598-172">**Mais informações**</span><span class="sxs-lookup"><span data-stu-id="fd598-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd598-173">Prompt</span><span class="sxs-lookup"><span data-stu-id="fd598-173">Prompt</span></span>  <br/> |<span data-ttu-id="fd598-174">Especifica um aviso descritivo ou comentário para a célula definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fd598-174">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |[<span data-ttu-id="fd598-175">Célula Prompt (Seção User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="fd598-175">Prompt Cell (User-Defined Cells Section)</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |
|<span data-ttu-id="fd598-176">Valor</span><span class="sxs-lookup"><span data-stu-id="fd598-176">Value</span></span>  <br/> |<span data-ttu-id="fd598-177">Especifica um valor para a célula correspondente definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fd598-177">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |[<span data-ttu-id="fd598-178">Célula Value (Seção User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="fd598-178">Value Cell (User-Defined Cells Section)</span></span>](value-cell-user-defined-cells-section.md) <br/> |
   

