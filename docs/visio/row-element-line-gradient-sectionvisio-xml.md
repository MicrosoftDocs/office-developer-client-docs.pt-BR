---
title: Elemento Row (seção line Gradient) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.
ms.openlocfilehash: 105d93344343f223a6b5d909f1174f7df56ffb4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358426"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="39332-103">Elemento Row (seção line Gradient) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="39332-103">Row element (Line Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="39332-104">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.</span><span class="sxs-lookup"><span data-stu-id="39332-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39332-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="39332-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39332-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="39332-106">**Element type**</span></span> <br/> |[<span data-ttu-id="39332-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="39332-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="39332-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="39332-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="39332-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="39332-109">**Schema file**</span></span> <br/> |<span data-ttu-id="39332-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="39332-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="39332-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="39332-111">**Document parts**</span></span> <br/> |<span data-ttu-id="39332-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="39332-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39332-113">Definição</span><span class="sxs-lookup"><span data-stu-id="39332-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39332-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="39332-114">Elements and attributes</span></span>

<span data-ttu-id="39332-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="39332-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="39332-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="39332-116">Parent elements</span></span>

|<span data-ttu-id="39332-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="39332-117">**Element**</span></span>|<span data-ttu-id="39332-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39332-118">**Type**</span></span>|<span data-ttu-id="39332-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39332-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39332-120">Section</span><span class="sxs-lookup"><span data-stu-id="39332-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="39332-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="39332-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39332-122">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.</span><span class="sxs-lookup"><span data-stu-id="39332-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39332-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="39332-123">Child elements</span></span>

|<span data-ttu-id="39332-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="39332-124">**Element**</span></span>|<span data-ttu-id="39332-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39332-125">**Type**</span></span>|<span data-ttu-id="39332-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39332-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39332-127">Cell</span><span class="sxs-lookup"><span data-stu-id="39332-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="39332-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="39332-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39332-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="39332-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="39332-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="39332-130">Attributes</span></span>

|<span data-ttu-id="39332-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="39332-131">**Attribute**</span></span>|<span data-ttu-id="39332-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39332-132">**Type**</span></span>|<span data-ttu-id="39332-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="39332-133">**Required**</span></span>|<span data-ttu-id="39332-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39332-134">**Description**</span></span>|<span data-ttu-id="39332-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="39332-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39332-136">Del</span><span class="sxs-lookup"><span data-stu-id="39332-136">Del</span></span>  <br/> |<span data-ttu-id="39332-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="39332-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="39332-138">opcional</span><span class="sxs-lookup"><span data-stu-id="39332-138">optional</span></span>  <br/> |<span data-ttu-id="39332-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="39332-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="39332-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="39332-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="39332-141">IX</span><span class="sxs-lookup"><span data-stu-id="39332-141">IX</span></span>  <br/> |<span data-ttu-id="39332-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="39332-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="39332-143">opcional</span><span class="sxs-lookup"><span data-stu-id="39332-143">optional</span></span>  <br/> |<span data-ttu-id="39332-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="39332-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="39332-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="39332-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="39332-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="39332-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="39332-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="39332-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="39332-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="39332-148">LocalName</span></span>  <br/> |<span data-ttu-id="39332-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="39332-149">xsd:string</span></span>  <br/> |<span data-ttu-id="39332-150">opcional</span><span class="sxs-lookup"><span data-stu-id="39332-150">optional</span></span>  <br/> |<span data-ttu-id="39332-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="39332-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="39332-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="39332-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="39332-153">N</span><span class="sxs-lookup"><span data-stu-id="39332-153">N</span></span>  <br/> |<span data-ttu-id="39332-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="39332-154">xsd:string</span></span>  <br/> |<span data-ttu-id="39332-155">opcional</span><span class="sxs-lookup"><span data-stu-id="39332-155">optional</span></span>  <br/> |<span data-ttu-id="39332-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="39332-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="39332-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="39332-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="39332-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="39332-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="39332-159">T</span><span class="sxs-lookup"><span data-stu-id="39332-159">T</span></span>  <br/> |<span data-ttu-id="39332-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="39332-160">xsd:string</span></span>  <br/> |<span data-ttu-id="39332-161">opcional</span><span class="sxs-lookup"><span data-stu-id="39332-161">optional</span></span>  <br/> |<span data-ttu-id="39332-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="39332-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="39332-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="39332-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="39332-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="39332-164">Values of the xsd:string type.</span></span>  <br/> |
   

