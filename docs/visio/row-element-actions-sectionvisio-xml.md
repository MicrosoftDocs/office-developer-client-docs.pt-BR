---
title: Elemento de linha (seção Actions) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388907"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="7bb40-103">Elemento de linha (seção Actions) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7bb40-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="7bb40-104">Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="7bb40-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bb40-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="7bb40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bb40-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7bb40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7bb40-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="7bb40-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7bb40-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7bb40-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7bb40-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7bb40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7bb40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7bb40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7bb40-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7bb40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7bb40-112">Masters.XML,. XML de # mestre, pages.xml,. XML n º de página</span><span class="sxs-lookup"><span data-stu-id="7bb40-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7bb40-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7bb40-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7bb40-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7bb40-114">Elements and attributes</span></span>

<span data-ttu-id="7bb40-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7bb40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7bb40-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7bb40-116">Parent elements</span></span>

|<span data-ttu-id="7bb40-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7bb40-117">**Element**</span></span>|<span data-ttu-id="7bb40-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7bb40-118">**Type**</span></span>|<span data-ttu-id="7bb40-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7bb40-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bb40-120">Seção</span><span class="sxs-lookup"><span data-stu-id="7bb40-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7bb40-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7bb40-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7bb40-122">Contém linhas que descrevem itens de menu em um menu de atalho ou marca de ação de uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="7bb40-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7bb40-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7bb40-123">Child elements</span></span>

|<span data-ttu-id="7bb40-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7bb40-124">**Element**</span></span>|<span data-ttu-id="7bb40-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7bb40-125">**Type**</span></span>|<span data-ttu-id="7bb40-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7bb40-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bb40-127">Célula</span><span class="sxs-lookup"><span data-stu-id="7bb40-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="7bb40-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7bb40-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7bb40-129">Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de atalho ou de ação de marca.</span><span class="sxs-lookup"><span data-stu-id="7bb40-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7bb40-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7bb40-130">Attributes</span></span>

|<span data-ttu-id="7bb40-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7bb40-131">**Attribute**</span></span>|<span data-ttu-id="7bb40-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7bb40-132">**Type**</span></span>|<span data-ttu-id="7bb40-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7bb40-133">**Required**</span></span>|<span data-ttu-id="7bb40-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7bb40-134">**Description**</span></span>|<span data-ttu-id="7bb40-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7bb40-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7bb40-136">DEL</span><span class="sxs-lookup"><span data-stu-id="7bb40-136">Del</span></span>  <br/> |<span data-ttu-id="7bb40-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="7bb40-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7bb40-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7bb40-138">optional</span></span>  <br/> |<span data-ttu-id="7bb40-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="7bb40-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="7bb40-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7bb40-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7bb40-141">IX</span><span class="sxs-lookup"><span data-stu-id="7bb40-141">IX</span></span>  <br/> |<span data-ttu-id="7bb40-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7bb40-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7bb40-143">opcional</span><span class="sxs-lookup"><span data-stu-id="7bb40-143">optional</span></span>  <br/> |<span data-ttu-id="7bb40-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="7bb40-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="7bb40-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="7bb40-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="7bb40-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7bb40-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7bb40-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7bb40-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7bb40-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="7bb40-148">LocalName</span></span>  <br/> |<span data-ttu-id="7bb40-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7bb40-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7bb40-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7bb40-150">optional</span></span>  <br/> |<span data-ttu-id="7bb40-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="7bb40-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="7bb40-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7bb40-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7bb40-153">N</span><span class="sxs-lookup"><span data-stu-id="7bb40-153">N</span></span>  <br/> |<span data-ttu-id="7bb40-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7bb40-154">xsd:string</span></span>  <br/> |<span data-ttu-id="7bb40-155">opcional</span><span class="sxs-lookup"><span data-stu-id="7bb40-155">optional</span></span>  <br/> |<span data-ttu-id="7bb40-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="7bb40-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="7bb40-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7bb40-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7bb40-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7bb40-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7bb40-159">T</span><span class="sxs-lookup"><span data-stu-id="7bb40-159">T</span></span>  <br/> |<span data-ttu-id="7bb40-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7bb40-160">xsd:string</span></span>  <br/> |<span data-ttu-id="7bb40-161">opcional</span><span class="sxs-lookup"><span data-stu-id="7bb40-161">optional</span></span>  <br/> |<span data-ttu-id="7bb40-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="7bb40-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="7bb40-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="7bb40-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="7bb40-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7bb40-164">Values of the xsd:string type.</span></span>  <br/> |
   

