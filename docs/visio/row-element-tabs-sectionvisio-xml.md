---
title: Elemento Row (Seção Tabs) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a30d5701-4b56-c44c-fb62-d9daaee3b86e
description: Contém as células para as formas ou os estilos que controlam o alinhamento e a posição de paradas de tabulação.
ms.openlocfilehash: 530d2e564615f33292b52f9aa860c0cf2794bc67
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538176"
---
# <a name="row-element-tabs-section-visio-xml"></a><span data-ttu-id="3ca19-103">Elemento Row (Seção Tabs) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3ca19-103">Row element (Tabs Section) (Visio XML)</span></span>

<span data-ttu-id="3ca19-104">Contém as células para as formas ou os estilos que controlam o alinhamento e a posição de paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3ca19-104">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ca19-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="3ca19-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ca19-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3ca19-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ca19-107">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="3ca19-107">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ca19-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ca19-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ca19-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ca19-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ca19-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3ca19-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ca19-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="3ca19-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ca19-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="3ca19-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ca19-113">Definição</span><span class="sxs-lookup"><span data-stu-id="3ca19-113">Definition</span></span>

```XML
< xs:element name="Row" type="TabsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ca19-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3ca19-114">Elements and attributes</span></span>

<span data-ttu-id="3ca19-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3ca19-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ca19-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3ca19-116">Parent elements</span></span>

|<span data-ttu-id="3ca19-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ca19-117">**Element**</span></span>|<span data-ttu-id="3ca19-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ca19-118">**Type**</span></span>|<span data-ttu-id="3ca19-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ca19-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ca19-120">Section</span><span class="sxs-lookup"><span data-stu-id="3ca19-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ca19-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="3ca19-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ca19-122">Contém as células para as formas ou os estilos que controlam o alinhamento e a posição de paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3ca19-122">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ca19-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ca19-123">Child elements</span></span>

|<span data-ttu-id="3ca19-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ca19-124">**Element**</span></span>|<span data-ttu-id="3ca19-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ca19-125">**Type**</span></span>|<span data-ttu-id="3ca19-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ca19-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ca19-127">Cell</span><span class="sxs-lookup"><span data-stu-id="3ca19-127">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="3ca19-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3ca19-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ca19-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="3ca19-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3ca19-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ca19-130">Attributes</span></span>

|<span data-ttu-id="3ca19-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3ca19-131">**Attribute**</span></span>|<span data-ttu-id="3ca19-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ca19-132">**Type**</span></span>|<span data-ttu-id="3ca19-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3ca19-133">**Required**</span></span>|<span data-ttu-id="3ca19-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ca19-134">**Description**</span></span>|<span data-ttu-id="3ca19-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3ca19-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ca19-136">Del</span><span class="sxs-lookup"><span data-stu-id="3ca19-136">Del</span></span>  <br/> |<span data-ttu-id="3ca19-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="3ca19-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3ca19-138">opcional</span><span class="sxs-lookup"><span data-stu-id="3ca19-138">optional</span></span>  <br/> |<span data-ttu-id="3ca19-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="3ca19-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="3ca19-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3ca19-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3ca19-141">IX</span><span class="sxs-lookup"><span data-stu-id="3ca19-141">IX</span></span>  <br/> |<span data-ttu-id="3ca19-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ca19-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ca19-143">opcional</span><span class="sxs-lookup"><span data-stu-id="3ca19-143">optional</span></span>  <br/> |<span data-ttu-id="3ca19-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="3ca19-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="3ca19-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="3ca19-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="3ca19-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="3ca19-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="3ca19-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ca19-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3ca19-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="3ca19-148">LocalName</span></span>  <br/> |<span data-ttu-id="3ca19-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3ca19-149">xsd:string</span></span>  <br/> |<span data-ttu-id="3ca19-150">opcional</span><span class="sxs-lookup"><span data-stu-id="3ca19-150">optional</span></span>  <br/> |<span data-ttu-id="3ca19-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="3ca19-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="3ca19-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ca19-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3ca19-153">N</span><span class="sxs-lookup"><span data-stu-id="3ca19-153">N</span></span>  <br/> |<span data-ttu-id="3ca19-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3ca19-154">xsd:string</span></span>  <br/> |<span data-ttu-id="3ca19-155">opcional</span><span class="sxs-lookup"><span data-stu-id="3ca19-155">optional</span></span>  <br/> |<span data-ttu-id="3ca19-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="3ca19-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="3ca19-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="3ca19-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="3ca19-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ca19-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3ca19-159">T</span><span class="sxs-lookup"><span data-stu-id="3ca19-159">T</span></span>  <br/> |<span data-ttu-id="3ca19-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3ca19-160">xsd:string</span></span>  <br/> |<span data-ttu-id="3ca19-161">opcional</span><span class="sxs-lookup"><span data-stu-id="3ca19-161">optional</span></span>  <br/> |<span data-ttu-id="3ca19-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="3ca19-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="3ca19-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="3ca19-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="3ca19-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ca19-164">Values of the xsd:string type.</span></span>  <br/> |
   

