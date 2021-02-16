---
title: Elemento Row (Seção Field) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
ms.openlocfilehash: c05f704610d7061b9e2c8b742adc39f2b72ba4ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541754"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="7b105-103">Elemento Row (Seção Field) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7b105-103">Row element (Field Section) (Visio XML)</span></span>

<span data-ttu-id="7b105-104">Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="7b105-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b105-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="7b105-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b105-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7b105-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7b105-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="7b105-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7b105-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7b105-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7b105-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7b105-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7b105-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7b105-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7b105-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7b105-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7b105-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="7b105-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b105-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7b105-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7b105-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7b105-114">Elements and attributes</span></span>

<span data-ttu-id="7b105-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7b105-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7b105-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7b105-116">Parent elements</span></span>

|<span data-ttu-id="7b105-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b105-117">**Element**</span></span>|<span data-ttu-id="7b105-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b105-118">**Type**</span></span>|<span data-ttu-id="7b105-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b105-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b105-120">Section</span><span class="sxs-lookup"><span data-stu-id="7b105-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b105-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7b105-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b105-122">Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="7b105-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b105-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7b105-123">Child elements</span></span>

|<span data-ttu-id="7b105-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b105-124">**Element**</span></span>|<span data-ttu-id="7b105-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b105-125">**Type**</span></span>|<span data-ttu-id="7b105-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b105-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b105-127">Cell</span><span class="sxs-lookup"><span data-stu-id="7b105-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7b105-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7b105-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b105-129">Exibe funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo</span><span class="sxs-lookup"><span data-stu-id="7b105-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7b105-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b105-130">Attributes</span></span>

|<span data-ttu-id="7b105-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7b105-131">**Attribute**</span></span>|<span data-ttu-id="7b105-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b105-132">**Type**</span></span>|<span data-ttu-id="7b105-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7b105-133">**Required**</span></span>|<span data-ttu-id="7b105-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b105-134">**Description**</span></span>|<span data-ttu-id="7b105-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7b105-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b105-136">Del</span><span class="sxs-lookup"><span data-stu-id="7b105-136">Del</span></span>  <br/> |<span data-ttu-id="7b105-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7b105-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7b105-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7b105-138">optional</span></span>  <br/> |<span data-ttu-id="7b105-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="7b105-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="7b105-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7b105-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7b105-141">IX</span><span class="sxs-lookup"><span data-stu-id="7b105-141">IX</span></span>  <br/> |<span data-ttu-id="7b105-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b105-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b105-143">opcional</span><span class="sxs-lookup"><span data-stu-id="7b105-143">optional</span></span>  <br/> |<span data-ttu-id="7b105-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="7b105-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="7b105-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="7b105-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="7b105-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7b105-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7b105-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b105-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b105-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="7b105-148">LocalName</span></span>  <br/> |<span data-ttu-id="7b105-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b105-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7b105-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7b105-150">optional</span></span>  <br/> |<span data-ttu-id="7b105-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="7b105-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="7b105-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b105-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b105-153">N</span><span class="sxs-lookup"><span data-stu-id="7b105-153">N</span></span>  <br/> |<span data-ttu-id="7b105-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b105-154">xsd:string</span></span>  <br/> |<span data-ttu-id="7b105-155">opcional</span><span class="sxs-lookup"><span data-stu-id="7b105-155">optional</span></span>  <br/> |<span data-ttu-id="7b105-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="7b105-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="7b105-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7b105-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7b105-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b105-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b105-159">T</span><span class="sxs-lookup"><span data-stu-id="7b105-159">T</span></span>  <br/> |<span data-ttu-id="7b105-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b105-160">xsd:string</span></span>  <br/> |<span data-ttu-id="7b105-161">opcional</span><span class="sxs-lookup"><span data-stu-id="7b105-161">optional</span></span>  <br/> |<span data-ttu-id="7b105-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="7b105-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="7b105-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="7b105-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="7b105-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b105-164">Values of the xsd:string type.</span></span>  <br/> |
   

