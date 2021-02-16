---
title: Elemento Row (Seção Scratch) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540998"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="2fc49-103">Elemento Row (Seção Scratch) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2fc49-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="2fc49-104">Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.</span><span class="sxs-lookup"><span data-stu-id="2fc49-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fc49-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="2fc49-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fc49-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2fc49-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2fc49-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="2fc49-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2fc49-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2fc49-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2fc49-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2fc49-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2fc49-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2fc49-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2fc49-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="2fc49-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2fc49-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="2fc49-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2fc49-113">Definição</span><span class="sxs-lookup"><span data-stu-id="2fc49-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2fc49-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2fc49-114">Elements and attributes</span></span>

<span data-ttu-id="2fc49-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2fc49-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2fc49-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2fc49-116">Parent elements</span></span>

|<span data-ttu-id="2fc49-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fc49-117">**Element**</span></span>|<span data-ttu-id="2fc49-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2fc49-118">**Type**</span></span>|<span data-ttu-id="2fc49-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fc49-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2fc49-120">Section</span><span class="sxs-lookup"><span data-stu-id="2fc49-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2fc49-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2fc49-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2fc49-122">Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.</span><span class="sxs-lookup"><span data-stu-id="2fc49-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2fc49-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2fc49-123">Child elements</span></span>

|<span data-ttu-id="2fc49-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fc49-124">**Element**</span></span>|<span data-ttu-id="2fc49-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2fc49-125">**Type**</span></span>|<span data-ttu-id="2fc49-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fc49-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2fc49-127">Cell</span><span class="sxs-lookup"><span data-stu-id="2fc49-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2fc49-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2fc49-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2fc49-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="2fc49-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2fc49-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="2fc49-130">Attributes</span></span>

|<span data-ttu-id="2fc49-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2fc49-131">**Attribute**</span></span>|<span data-ttu-id="2fc49-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2fc49-132">**Type**</span></span>|<span data-ttu-id="2fc49-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2fc49-133">**Required**</span></span>|<span data-ttu-id="2fc49-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fc49-134">**Description**</span></span>|<span data-ttu-id="2fc49-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2fc49-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2fc49-136">Del</span><span class="sxs-lookup"><span data-stu-id="2fc49-136">Del</span></span>  <br/> |<span data-ttu-id="2fc49-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2fc49-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2fc49-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2fc49-138">optional</span></span>  <br/> |<span data-ttu-id="2fc49-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="2fc49-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="2fc49-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2fc49-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2fc49-141">IX</span><span class="sxs-lookup"><span data-stu-id="2fc49-141">IX</span></span>  <br/> |<span data-ttu-id="2fc49-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2fc49-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2fc49-143">opcional</span><span class="sxs-lookup"><span data-stu-id="2fc49-143">optional</span></span>  <br/> |<span data-ttu-id="2fc49-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="2fc49-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="2fc49-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="2fc49-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="2fc49-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="2fc49-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2fc49-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2fc49-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2fc49-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="2fc49-148">LocalName</span></span>  <br/> |<span data-ttu-id="2fc49-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2fc49-149">xsd:string</span></span>  <br/> |<span data-ttu-id="2fc49-150">opcional</span><span class="sxs-lookup"><span data-stu-id="2fc49-150">optional</span></span>  <br/> |<span data-ttu-id="2fc49-151">Especifica o nome exclusivo dependente do idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="2fc49-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="2fc49-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2fc49-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2fc49-153">N</span><span class="sxs-lookup"><span data-stu-id="2fc49-153">N</span></span>  <br/> |<span data-ttu-id="2fc49-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2fc49-154">xsd:string</span></span>  <br/> |<span data-ttu-id="2fc49-155">opcional</span><span class="sxs-lookup"><span data-stu-id="2fc49-155">optional</span></span>  <br/> |<span data-ttu-id="2fc49-156">Especifica o nome exclusivo da linha independente do idioma. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="2fc49-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="2fc49-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="2fc49-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2fc49-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2fc49-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2fc49-159">T</span><span class="sxs-lookup"><span data-stu-id="2fc49-159">T</span></span>  <br/> |<span data-ttu-id="2fc49-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2fc49-160">xsd:string</span></span>  <br/> |<span data-ttu-id="2fc49-161">opcional</span><span class="sxs-lookup"><span data-stu-id="2fc49-161">optional</span></span>  <br/> |<span data-ttu-id="2fc49-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="2fc49-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="2fc49-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="2fc49-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="2fc49-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2fc49-164">Values of the xsd:string type.</span></span>  <br/> |
   

