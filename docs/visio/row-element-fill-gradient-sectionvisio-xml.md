---
title: Elemento Row (seção Fill Gradient) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538617"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="1b316-103">Elemento Row (seção Fill Gradient) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1b316-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="1b316-104">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="1b316-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b316-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="1b316-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b316-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1b316-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1b316-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="1b316-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1b316-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b316-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1b316-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1b316-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1b316-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1b316-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1b316-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1b316-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1b316-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="1b316-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b316-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1b316-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b316-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1b316-114">Elements and attributes</span></span>

<span data-ttu-id="1b316-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1b316-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b316-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1b316-116">Parent elements</span></span>

|<span data-ttu-id="1b316-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b316-117">**Element**</span></span>|<span data-ttu-id="1b316-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b316-118">**Type**</span></span>|<span data-ttu-id="1b316-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b316-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b316-120">Section</span><span class="sxs-lookup"><span data-stu-id="1b316-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b316-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1b316-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b316-122">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="1b316-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b316-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1b316-123">Child elements</span></span>

|<span data-ttu-id="1b316-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b316-124">**Element**</span></span>|<span data-ttu-id="1b316-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b316-125">**Type**</span></span>|<span data-ttu-id="1b316-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b316-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b316-127">Cell</span><span class="sxs-lookup"><span data-stu-id="1b316-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1b316-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1b316-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b316-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="1b316-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1b316-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b316-130">Attributes</span></span>

|<span data-ttu-id="1b316-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1b316-131">**Attribute**</span></span>|<span data-ttu-id="1b316-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b316-132">**Type**</span></span>|<span data-ttu-id="1b316-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1b316-133">**Required**</span></span>|<span data-ttu-id="1b316-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b316-134">**Description**</span></span>|<span data-ttu-id="1b316-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1b316-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b316-136">Del</span><span class="sxs-lookup"><span data-stu-id="1b316-136">Del</span></span>  <br/> |<span data-ttu-id="1b316-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1b316-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b316-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1b316-138">optional</span></span>  <br/> |<span data-ttu-id="1b316-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="1b316-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="1b316-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1b316-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1b316-141">IX</span><span class="sxs-lookup"><span data-stu-id="1b316-141">IX</span></span>  <br/> |<span data-ttu-id="1b316-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b316-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b316-143">opcional</span><span class="sxs-lookup"><span data-stu-id="1b316-143">optional</span></span>  <br/> |<span data-ttu-id="1b316-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="1b316-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="1b316-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="1b316-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="1b316-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="1b316-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1b316-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1b316-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b316-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="1b316-148">LocalName</span></span>  <br/> |<span data-ttu-id="1b316-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b316-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1b316-150">opcional</span><span class="sxs-lookup"><span data-stu-id="1b316-150">optional</span></span>  <br/> |<span data-ttu-id="1b316-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="1b316-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="1b316-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1b316-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b316-153">N</span><span class="sxs-lookup"><span data-stu-id="1b316-153">N</span></span>  <br/> |<span data-ttu-id="1b316-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b316-154">xsd:string</span></span>  <br/> |<span data-ttu-id="1b316-155">opcional</span><span class="sxs-lookup"><span data-stu-id="1b316-155">optional</span></span>  <br/> |<span data-ttu-id="1b316-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="1b316-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="1b316-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="1b316-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1b316-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1b316-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b316-159">T</span><span class="sxs-lookup"><span data-stu-id="1b316-159">T</span></span>  <br/> |<span data-ttu-id="1b316-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b316-160">xsd:string</span></span>  <br/> |<span data-ttu-id="1b316-161">opcional</span><span class="sxs-lookup"><span data-stu-id="1b316-161">optional</span></span>  <br/> |<span data-ttu-id="1b316-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="1b316-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="1b316-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="1b316-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="1b316-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1b316-164">Values of the xsd:string type.</span></span>  <br/> |
   

