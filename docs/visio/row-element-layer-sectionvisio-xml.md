---
title: Elemento de linha (seção Layer) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contém os elementos que definem uma única camada e suas propriedades para uma página.
ms.openlocfilehash: 2aff1666f5a2cb87ed10b76e0facdb19a4278c89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396838"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="34777-103">Elemento de linha (seção Layer) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="34777-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="34777-104">Contém os elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="34777-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34777-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="34777-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34777-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="34777-106">**Element type**</span></span> <br/> |[<span data-ttu-id="34777-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="34777-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="34777-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34777-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="34777-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="34777-109">**Schema file**</span></span> <br/> |<span data-ttu-id="34777-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="34777-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="34777-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="34777-111">**Document parts**</span></span> <br/> |<span data-ttu-id="34777-112">Masters.XML, pages.xml</span><span class="sxs-lookup"><span data-stu-id="34777-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34777-113">Definição</span><span class="sxs-lookup"><span data-stu-id="34777-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="34777-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="34777-114">Elements and attributes</span></span>

<span data-ttu-id="34777-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="34777-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="34777-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="34777-116">Parent elements</span></span>

|<span data-ttu-id="34777-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="34777-117">**Element**</span></span>|<span data-ttu-id="34777-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34777-118">**Type**</span></span>|<span data-ttu-id="34777-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34777-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34777-120">Seção</span><span class="sxs-lookup"><span data-stu-id="34777-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34777-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="34777-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34777-122">Contém os elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="34777-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="34777-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="34777-123">Child elements</span></span>

|<span data-ttu-id="34777-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="34777-124">**Element**</span></span>|<span data-ttu-id="34777-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34777-125">**Type**</span></span>|<span data-ttu-id="34777-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34777-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34777-127">Célula</span><span class="sxs-lookup"><span data-stu-id="34777-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="34777-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="34777-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34777-129">Especifica uma propriedade de uma camada, nem suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="34777-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="34777-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="34777-130">Attributes</span></span>

|<span data-ttu-id="34777-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="34777-131">**Attribute**</span></span>|<span data-ttu-id="34777-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34777-132">**Type**</span></span>|<span data-ttu-id="34777-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="34777-133">**Required**</span></span>|<span data-ttu-id="34777-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34777-134">**Description**</span></span>|<span data-ttu-id="34777-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="34777-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="34777-136">DEL</span><span class="sxs-lookup"><span data-stu-id="34777-136">Del</span></span>  <br/> |<span data-ttu-id="34777-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="34777-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="34777-138">opcional</span><span class="sxs-lookup"><span data-stu-id="34777-138">optional</span></span>  <br/> |<span data-ttu-id="34777-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="34777-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="34777-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="34777-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="34777-141">IX</span><span class="sxs-lookup"><span data-stu-id="34777-141">IX</span></span>  <br/> |<span data-ttu-id="34777-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34777-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34777-143">opcional</span><span class="sxs-lookup"><span data-stu-id="34777-143">optional</span></span>  <br/> |<span data-ttu-id="34777-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="34777-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="34777-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="34777-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="34777-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="34777-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="34777-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="34777-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34777-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="34777-148">LocalName</span></span>  <br/> |<span data-ttu-id="34777-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34777-149">xsd:string</span></span>  <br/> |<span data-ttu-id="34777-150">opcional</span><span class="sxs-lookup"><span data-stu-id="34777-150">optional</span></span>  <br/> |<span data-ttu-id="34777-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="34777-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="34777-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34777-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34777-153">N</span><span class="sxs-lookup"><span data-stu-id="34777-153">N</span></span>  <br/> |<span data-ttu-id="34777-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34777-154">xsd:string</span></span>  <br/> |<span data-ttu-id="34777-155">opcional</span><span class="sxs-lookup"><span data-stu-id="34777-155">optional</span></span>  <br/> |<span data-ttu-id="34777-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="34777-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="34777-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="34777-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="34777-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34777-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34777-159">T</span><span class="sxs-lookup"><span data-stu-id="34777-159">T</span></span>  <br/> |<span data-ttu-id="34777-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="34777-160">xsd:string</span></span>  <br/> |<span data-ttu-id="34777-161">opcional</span><span class="sxs-lookup"><span data-stu-id="34777-161">optional</span></span>  <br/> |<span data-ttu-id="34777-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="34777-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="34777-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="34777-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="34777-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34777-164">Values of the xsd:string type.</span></span>  <br/> |
   

