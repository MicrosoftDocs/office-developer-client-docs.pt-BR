---
title: Elemento Row (seção Layer) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contém elementos que definem uma única camada e suas propriedades para uma página.
ms.openlocfilehash: 2aff1666f5a2cb87ed10b76e0facdb19a4278c89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358447"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="19706-103">Elemento Row (seção Layer) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="19706-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="19706-104">Contém elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="19706-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19706-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="19706-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19706-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="19706-106">**Element type**</span></span> <br/> |[<span data-ttu-id="19706-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="19706-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="19706-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19706-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="19706-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="19706-109">**Schema file**</span></span> <br/> |<span data-ttu-id="19706-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="19706-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="19706-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="19706-111">**Document parts**</span></span> <br/> |<span data-ttu-id="19706-112">masters.xml, pages.xml</span><span class="sxs-lookup"><span data-stu-id="19706-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19706-113">Definição</span><span class="sxs-lookup"><span data-stu-id="19706-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="19706-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="19706-114">Elements and attributes</span></span>

<span data-ttu-id="19706-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="19706-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="19706-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="19706-116">Parent elements</span></span>

|<span data-ttu-id="19706-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="19706-117">**Element**</span></span>|<span data-ttu-id="19706-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19706-118">**Type**</span></span>|<span data-ttu-id="19706-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="19706-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19706-120">Section</span><span class="sxs-lookup"><span data-stu-id="19706-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19706-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="19706-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19706-122">Contém elementos que definem uma única camada e suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="19706-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="19706-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="19706-123">Child elements</span></span>

|<span data-ttu-id="19706-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="19706-124">**Element**</span></span>|<span data-ttu-id="19706-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19706-125">**Type**</span></span>|<span data-ttu-id="19706-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="19706-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19706-127">Cell</span><span class="sxs-lookup"><span data-stu-id="19706-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="19706-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="19706-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19706-129">Especifica uma propriedade para uma camada ou suas propriedades para uma página.</span><span class="sxs-lookup"><span data-stu-id="19706-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="19706-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="19706-130">Attributes</span></span>

|<span data-ttu-id="19706-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="19706-131">**Attribute**</span></span>|<span data-ttu-id="19706-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19706-132">**Type**</span></span>|<span data-ttu-id="19706-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="19706-133">**Required**</span></span>|<span data-ttu-id="19706-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="19706-134">**Description**</span></span>|<span data-ttu-id="19706-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="19706-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19706-136">Del</span><span class="sxs-lookup"><span data-stu-id="19706-136">Del</span></span>  <br/> |<span data-ttu-id="19706-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19706-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19706-138">opcional</span><span class="sxs-lookup"><span data-stu-id="19706-138">optional</span></span>  <br/> |<span data-ttu-id="19706-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="19706-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="19706-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19706-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19706-141">IX</span><span class="sxs-lookup"><span data-stu-id="19706-141">IX</span></span>  <br/> |<span data-ttu-id="19706-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19706-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19706-143">opcional</span><span class="sxs-lookup"><span data-stu-id="19706-143">optional</span></span>  <br/> |<span data-ttu-id="19706-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="19706-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="19706-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="19706-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="19706-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="19706-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="19706-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19706-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19706-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="19706-148">LocalName</span></span>  <br/> |<span data-ttu-id="19706-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19706-149">xsd:string</span></span>  <br/> |<span data-ttu-id="19706-150">opcional</span><span class="sxs-lookup"><span data-stu-id="19706-150">optional</span></span>  <br/> |<span data-ttu-id="19706-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="19706-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="19706-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19706-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19706-153">N</span><span class="sxs-lookup"><span data-stu-id="19706-153">N</span></span>  <br/> |<span data-ttu-id="19706-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19706-154">xsd:string</span></span>  <br/> |<span data-ttu-id="19706-155">opcional</span><span class="sxs-lookup"><span data-stu-id="19706-155">optional</span></span>  <br/> |<span data-ttu-id="19706-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="19706-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="19706-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="19706-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="19706-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19706-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19706-159">T</span><span class="sxs-lookup"><span data-stu-id="19706-159">T</span></span>  <br/> |<span data-ttu-id="19706-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19706-160">xsd:string</span></span>  <br/> |<span data-ttu-id="19706-161">opcional</span><span class="sxs-lookup"><span data-stu-id="19706-161">optional</span></span>  <br/> |<span data-ttu-id="19706-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="19706-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="19706-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="19706-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="19706-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19706-164">Values of the xsd:string type.</span></span>  <br/> |
   

