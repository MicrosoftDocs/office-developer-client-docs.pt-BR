---
title: Elemento Row (Seção Fill Gradient) (Visio XML)
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
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="9d46c-103">Elemento Row (Seção Fill Gradient) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9d46c-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="9d46c-104">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="9d46c-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d46c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9d46c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d46c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9d46c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9d46c-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="9d46c-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9d46c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d46c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9d46c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d46c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9d46c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9d46c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9d46c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9d46c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9d46c-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="9d46c-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d46c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9d46c-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d46c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9d46c-114">Elements and attributes</span></span>

<span data-ttu-id="9d46c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9d46c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d46c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9d46c-116">Parent elements</span></span>

|<span data-ttu-id="9d46c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d46c-117">**Element**</span></span>|<span data-ttu-id="9d46c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d46c-118">**Type**</span></span>|<span data-ttu-id="9d46c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d46c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d46c-120">Section</span><span class="sxs-lookup"><span data-stu-id="9d46c-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d46c-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9d46c-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d46c-122">Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="9d46c-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d46c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d46c-123">Child elements</span></span>

|<span data-ttu-id="9d46c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d46c-124">**Element**</span></span>|<span data-ttu-id="9d46c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d46c-125">**Type**</span></span>|<span data-ttu-id="9d46c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d46c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d46c-127">Cell</span><span class="sxs-lookup"><span data-stu-id="9d46c-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9d46c-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9d46c-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d46c-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="9d46c-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9d46c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d46c-130">Attributes</span></span>

|<span data-ttu-id="9d46c-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9d46c-131">**Attribute**</span></span>|<span data-ttu-id="9d46c-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d46c-132">**Type**</span></span>|<span data-ttu-id="9d46c-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9d46c-133">**Required**</span></span>|<span data-ttu-id="9d46c-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d46c-134">**Description**</span></span>|<span data-ttu-id="9d46c-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9d46c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d46c-136">Del</span><span class="sxs-lookup"><span data-stu-id="9d46c-136">Del</span></span>  <br/> |<span data-ttu-id="9d46c-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9d46c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9d46c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9d46c-138">optional</span></span>  <br/> |<span data-ttu-id="9d46c-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="9d46c-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="9d46c-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9d46c-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9d46c-141">IX</span><span class="sxs-lookup"><span data-stu-id="9d46c-141">IX</span></span>  <br/> |<span data-ttu-id="9d46c-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9d46c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9d46c-143">opcional</span><span class="sxs-lookup"><span data-stu-id="9d46c-143">optional</span></span>  <br/> |<span data-ttu-id="9d46c-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="9d46c-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="9d46c-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="9d46c-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="9d46c-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="9d46c-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9d46c-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9d46c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9d46c-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="9d46c-148">LocalName</span></span>  <br/> |<span data-ttu-id="9d46c-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d46c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9d46c-150">opcional</span><span class="sxs-lookup"><span data-stu-id="9d46c-150">optional</span></span>  <br/> |<span data-ttu-id="9d46c-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="9d46c-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="9d46c-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9d46c-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9d46c-153">N</span><span class="sxs-lookup"><span data-stu-id="9d46c-153">N</span></span>  <br/> |<span data-ttu-id="9d46c-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d46c-154">xsd:string</span></span>  <br/> |<span data-ttu-id="9d46c-155">opcional</span><span class="sxs-lookup"><span data-stu-id="9d46c-155">optional</span></span>  <br/> |<span data-ttu-id="9d46c-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="9d46c-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="9d46c-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="9d46c-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9d46c-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9d46c-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9d46c-159">T</span><span class="sxs-lookup"><span data-stu-id="9d46c-159">T</span></span>  <br/> |<span data-ttu-id="9d46c-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d46c-160">xsd:string</span></span>  <br/> |<span data-ttu-id="9d46c-161">opcional</span><span class="sxs-lookup"><span data-stu-id="9d46c-161">optional</span></span>  <br/> |<span data-ttu-id="9d46c-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="9d46c-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="9d46c-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="9d46c-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="9d46c-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9d46c-164">Values of the xsd:string type.</span></span>  <br/> |
   

