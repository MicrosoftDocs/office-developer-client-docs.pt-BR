---
title: Elemento de linha (seção Shape Data) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica uma entrada de dados de forma para associar os dados uma forma.
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385505"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="09a87-103">Elemento de linha (seção Shape Data) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="09a87-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="09a87-104">Especifica uma entrada de dados de forma para associar os dados uma forma.</span><span class="sxs-lookup"><span data-stu-id="09a87-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09a87-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="09a87-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09a87-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="09a87-106">**Element type**</span></span> <br/> |[<span data-ttu-id="09a87-107">Forma Data_Type</span><span class="sxs-lookup"><span data-stu-id="09a87-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="09a87-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="09a87-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="09a87-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="09a87-109">**Schema file**</span></span> <br/> |<span data-ttu-id="09a87-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="09a87-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="09a87-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="09a87-111">**Document parts**</span></span> <br/> |<span data-ttu-id="09a87-112"># XML do mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="09a87-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09a87-113">Definição</span><span class="sxs-lookup"><span data-stu-id="09a87-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09a87-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="09a87-114">Elements and attributes</span></span>

<span data-ttu-id="09a87-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="09a87-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="09a87-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="09a87-116">Parent elements</span></span>

|<span data-ttu-id="09a87-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09a87-117">**Element**</span></span>|<span data-ttu-id="09a87-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="09a87-118">**Type**</span></span>|<span data-ttu-id="09a87-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09a87-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09a87-120">Seção</span><span class="sxs-lookup"><span data-stu-id="09a87-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09a87-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="09a87-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09a87-122">Especifica uma entrada de dados de forma para associar os dados uma forma.</span><span class="sxs-lookup"><span data-stu-id="09a87-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="09a87-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="09a87-123">Child elements</span></span>

|<span data-ttu-id="09a87-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09a87-124">**Element**</span></span>|<span data-ttu-id="09a87-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="09a87-125">**Type**</span></span>|<span data-ttu-id="09a87-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09a87-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09a87-127">Célula</span><span class="sxs-lookup"><span data-stu-id="09a87-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="09a87-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="09a87-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09a87-129">Especifica uma propriedade dos dados da forma.</span><span class="sxs-lookup"><span data-stu-id="09a87-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="09a87-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="09a87-130">Attributes</span></span>

|<span data-ttu-id="09a87-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="09a87-131">**Attribute**</span></span>|<span data-ttu-id="09a87-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="09a87-132">**Type**</span></span>|<span data-ttu-id="09a87-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="09a87-133">**Required**</span></span>|<span data-ttu-id="09a87-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09a87-134">**Description**</span></span>|<span data-ttu-id="09a87-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="09a87-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09a87-136">DEL</span><span class="sxs-lookup"><span data-stu-id="09a87-136">Del</span></span>  <br/> |<span data-ttu-id="09a87-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="09a87-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="09a87-138">opcional</span><span class="sxs-lookup"><span data-stu-id="09a87-138">optional</span></span>  <br/> |<span data-ttu-id="09a87-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="09a87-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="09a87-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="09a87-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="09a87-141">IX</span><span class="sxs-lookup"><span data-stu-id="09a87-141">IX</span></span>  <br/> |<span data-ttu-id="09a87-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09a87-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09a87-143">opcional</span><span class="sxs-lookup"><span data-stu-id="09a87-143">optional</span></span>  <br/> |<span data-ttu-id="09a87-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="09a87-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="09a87-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="09a87-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="09a87-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="09a87-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="09a87-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09a87-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09a87-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="09a87-148">LocalName</span></span>  <br/> |<span data-ttu-id="09a87-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="09a87-149">xsd:string</span></span>  <br/> |<span data-ttu-id="09a87-150">opcional</span><span class="sxs-lookup"><span data-stu-id="09a87-150">optional</span></span>  <br/> |<span data-ttu-id="09a87-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="09a87-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="09a87-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="09a87-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09a87-153">N</span><span class="sxs-lookup"><span data-stu-id="09a87-153">N</span></span>  <br/> |<span data-ttu-id="09a87-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="09a87-154">xsd:string</span></span>  <br/> |<span data-ttu-id="09a87-155">opcional</span><span class="sxs-lookup"><span data-stu-id="09a87-155">optional</span></span>  <br/> |<span data-ttu-id="09a87-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="09a87-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="09a87-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="09a87-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="09a87-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="09a87-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09a87-159">T</span><span class="sxs-lookup"><span data-stu-id="09a87-159">T</span></span>  <br/> |<span data-ttu-id="09a87-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="09a87-160">xsd:string</span></span>  <br/> |<span data-ttu-id="09a87-161">opcional</span><span class="sxs-lookup"><span data-stu-id="09a87-161">optional</span></span>  <br/> |<span data-ttu-id="09a87-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="09a87-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="09a87-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="09a87-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="09a87-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="09a87-164">Values of the xsd:string type.</span></span>  <br/> |
   

