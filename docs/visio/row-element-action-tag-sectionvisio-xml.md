---
title: Elemento de linha (seção marca de ação) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Define uma marca de ação em uma forma ou página.
ms.openlocfilehash: 1e5e432b05b1dfcd02dded41253a79802c9caf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772760"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="30248-103">Elemento de linha (seção marca de ação) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="30248-103">Row element (Action Tag Section) ('Visio XML')</span></span>

<span data-ttu-id="30248-104">Define uma marca de ação em uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="30248-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30248-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="30248-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30248-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="30248-106">**Element type**</span></span> <br/> |[<span data-ttu-id="30248-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="30248-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="30248-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30248-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="30248-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="30248-109">**Schema file**</span></span> <br/> |<span data-ttu-id="30248-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="30248-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="30248-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="30248-111">**Document parts**</span></span> <br/> |<span data-ttu-id="30248-112">Masters.XML,. XML de # mestre, pages.xml,. XML n º de página</span><span class="sxs-lookup"><span data-stu-id="30248-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30248-113">Definição</span><span class="sxs-lookup"><span data-stu-id="30248-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="30248-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="30248-114">Elements and attributes</span></span>

<span data-ttu-id="30248-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="30248-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="30248-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="30248-116">Parent elements</span></span>

|<span data-ttu-id="30248-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="30248-117">**Element**</span></span>|<span data-ttu-id="30248-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30248-118">**Type**</span></span>|<span data-ttu-id="30248-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30248-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30248-120">Seção</span><span class="sxs-lookup"><span data-stu-id="30248-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30248-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="30248-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30248-122">Define uma marca de ação em uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="30248-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30248-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="30248-123">Child elements</span></span>

|<span data-ttu-id="30248-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="30248-124">**Element**</span></span>|<span data-ttu-id="30248-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30248-125">**Type**</span></span>|<span data-ttu-id="30248-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30248-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30248-127">Célula</span><span class="sxs-lookup"><span data-stu-id="30248-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="30248-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="30248-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30248-129">Define uma propriedade para uma marca de ação em uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="30248-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="30248-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="30248-130">Attributes</span></span>

|<span data-ttu-id="30248-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="30248-131">**Attribute**</span></span>|<span data-ttu-id="30248-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30248-132">**Type**</span></span>|<span data-ttu-id="30248-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="30248-133">**Required**</span></span>|<span data-ttu-id="30248-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30248-134">**Description**</span></span>|<span data-ttu-id="30248-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="30248-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30248-136">DEL</span><span class="sxs-lookup"><span data-stu-id="30248-136">Del</span></span>  <br/> |<span data-ttu-id="30248-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="30248-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30248-138">opcional</span><span class="sxs-lookup"><span data-stu-id="30248-138">optional</span></span>  <br/> |<span data-ttu-id="30248-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="30248-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="30248-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="30248-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="30248-141">IX</span><span class="sxs-lookup"><span data-stu-id="30248-141">IX</span></span>  <br/> |<span data-ttu-id="30248-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30248-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30248-143">opcional</span><span class="sxs-lookup"><span data-stu-id="30248-143">optional</span></span>  <br/> |<span data-ttu-id="30248-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="30248-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="30248-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="30248-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="30248-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="30248-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="30248-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="30248-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30248-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="30248-148">LocalName</span></span>  <br/> |<span data-ttu-id="30248-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30248-149">xsd:string</span></span>  <br/> |<span data-ttu-id="30248-150">opcional</span><span class="sxs-lookup"><span data-stu-id="30248-150">optional</span></span>  <br/> |<span data-ttu-id="30248-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="30248-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="30248-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30248-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30248-153">N</span><span class="sxs-lookup"><span data-stu-id="30248-153">N</span></span>  <br/> |<span data-ttu-id="30248-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30248-154">xsd:string</span></span>  <br/> |<span data-ttu-id="30248-155">opcional</span><span class="sxs-lookup"><span data-stu-id="30248-155">optional</span></span>  <br/> |<span data-ttu-id="30248-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="30248-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="30248-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="30248-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="30248-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30248-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30248-159">T</span><span class="sxs-lookup"><span data-stu-id="30248-159">T</span></span>  <br/> |<span data-ttu-id="30248-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30248-160">xsd:string</span></span>  <br/> |<span data-ttu-id="30248-161">opcional</span><span class="sxs-lookup"><span data-stu-id="30248-161">optional</span></span>  <br/> |<span data-ttu-id="30248-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="30248-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="30248-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="30248-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="30248-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30248-164">Values of the xsd:string type.</span></span>  <br/> |
   

