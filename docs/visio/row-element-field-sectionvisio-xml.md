---
title: Elemento de linha (seção de campo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
ms.openlocfilehash: ec01ae3743eaf5345685c7273404bfdb826579ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772787"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="38dab-103">Elemento de linha (seção de campo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="38dab-103">Row element (Field Section) ('Visio XML')</span></span>

<span data-ttu-id="38dab-104">Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="38dab-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38dab-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="38dab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38dab-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="38dab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="38dab-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="38dab-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="38dab-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38dab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="38dab-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="38dab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="38dab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="38dab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="38dab-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="38dab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="38dab-112"># XML do mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="38dab-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38dab-113">Definição</span><span class="sxs-lookup"><span data-stu-id="38dab-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="38dab-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="38dab-114">Elements and attributes</span></span>

<span data-ttu-id="38dab-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="38dab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="38dab-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="38dab-116">Parent elements</span></span>

|<span data-ttu-id="38dab-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="38dab-117">**Element**</span></span>|<span data-ttu-id="38dab-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38dab-118">**Type**</span></span>|<span data-ttu-id="38dab-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38dab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38dab-120">Seção</span><span class="sxs-lookup"><span data-stu-id="38dab-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="38dab-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="38dab-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="38dab-122">Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.</span><span class="sxs-lookup"><span data-stu-id="38dab-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38dab-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="38dab-123">Child elements</span></span>

|<span data-ttu-id="38dab-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="38dab-124">**Element**</span></span>|<span data-ttu-id="38dab-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38dab-125">**Type**</span></span>|<span data-ttu-id="38dab-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38dab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38dab-127">Célula</span><span class="sxs-lookup"><span data-stu-id="38dab-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="38dab-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="38dab-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="38dab-129">Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo campo</span><span class="sxs-lookup"><span data-stu-id="38dab-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="38dab-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="38dab-130">Attributes</span></span>

|<span data-ttu-id="38dab-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="38dab-131">**Attribute**</span></span>|<span data-ttu-id="38dab-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38dab-132">**Type**</span></span>|<span data-ttu-id="38dab-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="38dab-133">**Required**</span></span>|<span data-ttu-id="38dab-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38dab-134">**Description**</span></span>|<span data-ttu-id="38dab-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="38dab-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38dab-136">DEL</span><span class="sxs-lookup"><span data-stu-id="38dab-136">Del</span></span>  <br/> |<span data-ttu-id="38dab-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="38dab-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="38dab-138">opcional</span><span class="sxs-lookup"><span data-stu-id="38dab-138">optional</span></span>  <br/> |<span data-ttu-id="38dab-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="38dab-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="38dab-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="38dab-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="38dab-141">IX</span><span class="sxs-lookup"><span data-stu-id="38dab-141">IX</span></span>  <br/> |<span data-ttu-id="38dab-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="38dab-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="38dab-143">opcional</span><span class="sxs-lookup"><span data-stu-id="38dab-143">optional</span></span>  <br/> |<span data-ttu-id="38dab-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="38dab-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="38dab-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="38dab-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="38dab-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="38dab-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="38dab-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="38dab-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="38dab-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="38dab-148">LocalName</span></span>  <br/> |<span data-ttu-id="38dab-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="38dab-149">xsd:string</span></span>  <br/> |<span data-ttu-id="38dab-150">opcional</span><span class="sxs-lookup"><span data-stu-id="38dab-150">optional</span></span>  <br/> |<span data-ttu-id="38dab-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="38dab-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="38dab-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="38dab-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38dab-153">N</span><span class="sxs-lookup"><span data-stu-id="38dab-153">N</span></span>  <br/> |<span data-ttu-id="38dab-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="38dab-154">xsd:string</span></span>  <br/> |<span data-ttu-id="38dab-155">opcional</span><span class="sxs-lookup"><span data-stu-id="38dab-155">optional</span></span>  <br/> |<span data-ttu-id="38dab-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="38dab-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="38dab-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="38dab-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="38dab-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="38dab-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38dab-159">T</span><span class="sxs-lookup"><span data-stu-id="38dab-159">T</span></span>  <br/> |<span data-ttu-id="38dab-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="38dab-160">xsd:string</span></span>  <br/> |<span data-ttu-id="38dab-161">opcional</span><span class="sxs-lookup"><span data-stu-id="38dab-161">optional</span></span>  <br/> |<span data-ttu-id="38dab-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="38dab-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="38dab-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="38dab-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="38dab-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="38dab-164">Values of the xsd:string type.</span></span>  <br/> |
   

