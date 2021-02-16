---
title: Elemento Row (Seção Actions) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.
ms.openlocfilehash: dfe23aa7d635fc09d625c414e5548a0166384fbb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540410"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="9a839-103">Elemento Row (Seção Actions) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9a839-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="9a839-104">Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="9a839-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a839-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9a839-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a839-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9a839-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9a839-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="9a839-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9a839-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a839-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9a839-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9a839-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9a839-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9a839-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9a839-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9a839-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9a839-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="9a839-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a839-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9a839-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a839-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9a839-114">Elements and attributes</span></span>

<span data-ttu-id="9a839-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9a839-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9a839-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9a839-116">Parent elements</span></span>

|<span data-ttu-id="9a839-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a839-117">**Element**</span></span>|<span data-ttu-id="9a839-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a839-118">**Type**</span></span>|<span data-ttu-id="9a839-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a839-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a839-120">Section</span><span class="sxs-lookup"><span data-stu-id="9a839-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a839-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9a839-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a839-122">Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="9a839-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9a839-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9a839-123">Child elements</span></span>

|<span data-ttu-id="9a839-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a839-124">**Element**</span></span>|<span data-ttu-id="9a839-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a839-125">**Type**</span></span>|<span data-ttu-id="9a839-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a839-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a839-127">Cell</span><span class="sxs-lookup"><span data-stu-id="9a839-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="9a839-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9a839-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a839-129">Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de marca de ação ou atalho.</span><span class="sxs-lookup"><span data-stu-id="9a839-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9a839-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a839-130">Attributes</span></span>

|<span data-ttu-id="9a839-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9a839-131">**Attribute**</span></span>|<span data-ttu-id="9a839-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a839-132">**Type**</span></span>|<span data-ttu-id="9a839-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9a839-133">**Required**</span></span>|<span data-ttu-id="9a839-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a839-134">**Description**</span></span>|<span data-ttu-id="9a839-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9a839-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a839-136">Del</span><span class="sxs-lookup"><span data-stu-id="9a839-136">Del</span></span>  <br/> |<span data-ttu-id="9a839-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a839-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a839-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9a839-138">optional</span></span>  <br/> |<span data-ttu-id="9a839-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="9a839-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="9a839-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a839-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a839-141">IX</span><span class="sxs-lookup"><span data-stu-id="9a839-141">IX</span></span>  <br/> |<span data-ttu-id="9a839-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a839-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a839-143">opcional</span><span class="sxs-lookup"><span data-stu-id="9a839-143">optional</span></span>  <br/> |<span data-ttu-id="9a839-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="9a839-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="9a839-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="9a839-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="9a839-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="9a839-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9a839-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a839-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a839-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="9a839-148">LocalName</span></span>  <br/> |<span data-ttu-id="9a839-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a839-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9a839-150">opcional</span><span class="sxs-lookup"><span data-stu-id="9a839-150">optional</span></span>  <br/> |<span data-ttu-id="9a839-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="9a839-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="9a839-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a839-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a839-153">N</span><span class="sxs-lookup"><span data-stu-id="9a839-153">N</span></span>  <br/> |<span data-ttu-id="9a839-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a839-154">xsd:string</span></span>  <br/> |<span data-ttu-id="9a839-155">opcional</span><span class="sxs-lookup"><span data-stu-id="9a839-155">optional</span></span>  <br/> |<span data-ttu-id="9a839-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="9a839-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="9a839-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="9a839-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9a839-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a839-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a839-159">T</span><span class="sxs-lookup"><span data-stu-id="9a839-159">T</span></span>  <br/> |<span data-ttu-id="9a839-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a839-160">xsd:string</span></span>  <br/> |<span data-ttu-id="9a839-161">opcional</span><span class="sxs-lookup"><span data-stu-id="9a839-161">optional</span></span>  <br/> |<span data-ttu-id="9a839-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="9a839-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="9a839-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="9a839-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="9a839-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a839-164">Values of the xsd:string type.</span></span>  <br/> |
   

