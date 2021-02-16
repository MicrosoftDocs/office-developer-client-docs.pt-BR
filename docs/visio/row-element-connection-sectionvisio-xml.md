---
title: Elemento Row (Seção Connection) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Contém as coordenadas x ou y, a direção horizontal e vertical e o tipo do ponto de conexão único em uma forma.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541761"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="26503-103">Elemento Row (Seção Connection) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="26503-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="26503-104">Contém as coordenadas x ou y, a direção horizontal e vertical e o tipo do ponto de conexão único em uma forma.</span><span class="sxs-lookup"><span data-stu-id="26503-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26503-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="26503-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26503-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="26503-106">**Element type**</span></span> <br/> |[<span data-ttu-id="26503-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="26503-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="26503-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26503-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="26503-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="26503-109">**Schema file**</span></span> <br/> |<span data-ttu-id="26503-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="26503-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="26503-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="26503-111">**Document parts**</span></span> <br/> |<span data-ttu-id="26503-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="26503-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26503-113">Definição</span><span class="sxs-lookup"><span data-stu-id="26503-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26503-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="26503-114">Elements and attributes</span></span>

<span data-ttu-id="26503-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="26503-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="26503-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="26503-116">Parent elements</span></span>

|<span data-ttu-id="26503-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26503-117">**Element**</span></span>|<span data-ttu-id="26503-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26503-118">**Type**</span></span>|<span data-ttu-id="26503-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26503-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26503-120">Section</span><span class="sxs-lookup"><span data-stu-id="26503-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26503-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="26503-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26503-122">Contém as coordenadas x ou y, a direção horizontal e vertical e o tipo do ponto de conexão único em uma forma.</span><span class="sxs-lookup"><span data-stu-id="26503-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26503-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="26503-123">Child elements</span></span>

|<span data-ttu-id="26503-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26503-124">**Element**</span></span>|<span data-ttu-id="26503-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26503-125">**Type**</span></span>|<span data-ttu-id="26503-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26503-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26503-127">Cell</span><span class="sxs-lookup"><span data-stu-id="26503-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="26503-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="26503-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26503-129">Especifica uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="26503-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="26503-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="26503-130">Attributes</span></span>

|<span data-ttu-id="26503-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="26503-131">**Attribute**</span></span>|<span data-ttu-id="26503-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26503-132">**Type**</span></span>|<span data-ttu-id="26503-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="26503-133">**Required**</span></span>|<span data-ttu-id="26503-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26503-134">**Description**</span></span>|<span data-ttu-id="26503-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="26503-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26503-136">Del</span><span class="sxs-lookup"><span data-stu-id="26503-136">Del</span></span>  <br/> |<span data-ttu-id="26503-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="26503-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="26503-138">opcional</span><span class="sxs-lookup"><span data-stu-id="26503-138">optional</span></span>  <br/> |<span data-ttu-id="26503-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="26503-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="26503-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="26503-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="26503-141">IX</span><span class="sxs-lookup"><span data-stu-id="26503-141">IX</span></span>  <br/> |<span data-ttu-id="26503-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="26503-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="26503-143">opcional</span><span class="sxs-lookup"><span data-stu-id="26503-143">optional</span></span>  <br/> |<span data-ttu-id="26503-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="26503-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="26503-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="26503-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="26503-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="26503-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="26503-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="26503-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="26503-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="26503-148">LocalName</span></span>  <br/> |<span data-ttu-id="26503-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26503-149">xsd:string</span></span>  <br/> |<span data-ttu-id="26503-150">opcional</span><span class="sxs-lookup"><span data-stu-id="26503-150">optional</span></span>  <br/> |<span data-ttu-id="26503-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="26503-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="26503-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="26503-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="26503-153">N</span><span class="sxs-lookup"><span data-stu-id="26503-153">N</span></span>  <br/> |<span data-ttu-id="26503-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26503-154">xsd:string</span></span>  <br/> |<span data-ttu-id="26503-155">opcional</span><span class="sxs-lookup"><span data-stu-id="26503-155">optional</span></span>  <br/> |<span data-ttu-id="26503-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="26503-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="26503-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="26503-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="26503-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="26503-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="26503-159">T</span><span class="sxs-lookup"><span data-stu-id="26503-159">T</span></span>  <br/> |<span data-ttu-id="26503-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="26503-160">xsd:string</span></span>  <br/> |<span data-ttu-id="26503-161">opcional</span><span class="sxs-lookup"><span data-stu-id="26503-161">optional</span></span>  <br/> |<span data-ttu-id="26503-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="26503-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="26503-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="26503-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="26503-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="26503-164">Values of the xsd:string type.</span></span>  <br/> |
   

