---
title: Elemento Row (seção Layer) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contém elementos que definem uma única camada e suas propriedades para uma página.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540859"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="16fd0-103">Elemento Row (seção Layer) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="16fd0-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="16fd0-104">Contém elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="16fd0-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16fd0-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="16fd0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16fd0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="16fd0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="16fd0-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="16fd0-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="16fd0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="16fd0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="16fd0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="16fd0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="16fd0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="16fd0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="16fd0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="16fd0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="16fd0-112">masters.xml, pages.xml</span><span class="sxs-lookup"><span data-stu-id="16fd0-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16fd0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="16fd0-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="16fd0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="16fd0-114">Elements and attributes</span></span>

<span data-ttu-id="16fd0-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="16fd0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="16fd0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="16fd0-116">Parent elements</span></span>

|<span data-ttu-id="16fd0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16fd0-117">**Element**</span></span>|<span data-ttu-id="16fd0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16fd0-118">**Type**</span></span>|<span data-ttu-id="16fd0-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="16fd0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16fd0-120">Section</span><span class="sxs-lookup"><span data-stu-id="16fd0-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16fd0-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="16fd0-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16fd0-122">Contém elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="16fd0-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16fd0-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="16fd0-123">Child elements</span></span>

|<span data-ttu-id="16fd0-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16fd0-124">**Element**</span></span>|<span data-ttu-id="16fd0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16fd0-125">**Type**</span></span>|<span data-ttu-id="16fd0-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="16fd0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16fd0-127">Cell</span><span class="sxs-lookup"><span data-stu-id="16fd0-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="16fd0-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="16fd0-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16fd0-129">Especifica uma propriedade para uma camada ou suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="16fd0-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="16fd0-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="16fd0-130">Attributes</span></span>

|<span data-ttu-id="16fd0-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="16fd0-131">**Attribute**</span></span>|<span data-ttu-id="16fd0-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16fd0-132">**Type**</span></span>|<span data-ttu-id="16fd0-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="16fd0-133">**Required**</span></span>|<span data-ttu-id="16fd0-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="16fd0-134">**Description**</span></span>|<span data-ttu-id="16fd0-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="16fd0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="16fd0-136">Del</span><span class="sxs-lookup"><span data-stu-id="16fd0-136">Del</span></span>  <br/> |<span data-ttu-id="16fd0-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="16fd0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="16fd0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="16fd0-138">optional</span></span>  <br/> |<span data-ttu-id="16fd0-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="16fd0-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="16fd0-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="16fd0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="16fd0-141">IX</span><span class="sxs-lookup"><span data-stu-id="16fd0-141">IX</span></span>  <br/> |<span data-ttu-id="16fd0-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="16fd0-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="16fd0-143">opcional</span><span class="sxs-lookup"><span data-stu-id="16fd0-143">optional</span></span>  <br/> |<span data-ttu-id="16fd0-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="16fd0-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="16fd0-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="16fd0-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="16fd0-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="16fd0-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="16fd0-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="16fd0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="16fd0-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="16fd0-148">LocalName</span></span>  <br/> |<span data-ttu-id="16fd0-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="16fd0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="16fd0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="16fd0-150">optional</span></span>  <br/> |<span data-ttu-id="16fd0-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="16fd0-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="16fd0-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="16fd0-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16fd0-153">N</span><span class="sxs-lookup"><span data-stu-id="16fd0-153">N</span></span>  <br/> |<span data-ttu-id="16fd0-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="16fd0-154">xsd:string</span></span>  <br/> |<span data-ttu-id="16fd0-155">opcional</span><span class="sxs-lookup"><span data-stu-id="16fd0-155">optional</span></span>  <br/> |<span data-ttu-id="16fd0-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="16fd0-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="16fd0-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="16fd0-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="16fd0-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="16fd0-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16fd0-159">T</span><span class="sxs-lookup"><span data-stu-id="16fd0-159">T</span></span>  <br/> |<span data-ttu-id="16fd0-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="16fd0-160">xsd:string</span></span>  <br/> |<span data-ttu-id="16fd0-161">opcional</span><span class="sxs-lookup"><span data-stu-id="16fd0-161">optional</span></span>  <br/> |<span data-ttu-id="16fd0-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="16fd0-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="16fd0-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="16fd0-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="16fd0-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="16fd0-164">Values of the xsd:string type.</span></span>  <br/> |
   

