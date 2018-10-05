---
title: Elemento de linha (seção de células definidas pelo usuário) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Uma parte das informações que podem ser referenciadas por outras células e outras ferramentas de complemento especificados pelo usuário.
ms.openlocfilehash: 8852c1db31e9a9b8f0860c111da32de6d44dc7f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388011"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="acf34-103">Elemento de linha (seção de células definidas pelo usuário) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="acf34-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="acf34-104">Uma parte das informações que podem ser referenciadas por outras células e outras ferramentas de complemento especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="acf34-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acf34-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="acf34-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acf34-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="acf34-106">**Element type**</span></span> <br/> |[<span data-ttu-id="acf34-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="acf34-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="acf34-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acf34-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="acf34-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="acf34-109">**Schema file**</span></span> <br/> |<span data-ttu-id="acf34-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="acf34-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="acf34-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="acf34-111">**Document parts**</span></span> <br/> |<span data-ttu-id="acf34-112">Document, masters.xml,. XML de # mestre, pages.xml,. XML n º de página</span><span class="sxs-lookup"><span data-stu-id="acf34-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acf34-113">Definição</span><span class="sxs-lookup"><span data-stu-id="acf34-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acf34-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="acf34-114">Elements and attributes</span></span>

<span data-ttu-id="acf34-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="acf34-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="acf34-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="acf34-116">Parent elements</span></span>

|<span data-ttu-id="acf34-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acf34-117">**Element**</span></span>|<span data-ttu-id="acf34-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acf34-118">**Type**</span></span>|<span data-ttu-id="acf34-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acf34-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acf34-120">Seção</span><span class="sxs-lookup"><span data-stu-id="acf34-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acf34-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="acf34-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acf34-122">Uma parte das informações que podem ser referenciadas por outras células e outras ferramentas de complemento especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="acf34-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="acf34-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="acf34-123">Child elements</span></span>

|<span data-ttu-id="acf34-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acf34-124">**Element**</span></span>|<span data-ttu-id="acf34-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acf34-125">**Type**</span></span>|<span data-ttu-id="acf34-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acf34-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acf34-127">Célula</span><span class="sxs-lookup"><span data-stu-id="acf34-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="acf34-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="acf34-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acf34-129">Uma propriedade de uma parte especificada pelo usuário de informações que podem ser referenciadas por outras células e outras ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="acf34-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="acf34-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="acf34-130">Attributes</span></span>

|<span data-ttu-id="acf34-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="acf34-131">**Attribute**</span></span>|<span data-ttu-id="acf34-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acf34-132">**Type**</span></span>|<span data-ttu-id="acf34-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="acf34-133">**Required**</span></span>|<span data-ttu-id="acf34-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acf34-134">**Description**</span></span>|<span data-ttu-id="acf34-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="acf34-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="acf34-136">DEL</span><span class="sxs-lookup"><span data-stu-id="acf34-136">Del</span></span>  <br/> |<span data-ttu-id="acf34-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="acf34-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="acf34-138">opcional</span><span class="sxs-lookup"><span data-stu-id="acf34-138">optional</span></span>  <br/> |<span data-ttu-id="acf34-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="acf34-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="acf34-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="acf34-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="acf34-141">IX</span><span class="sxs-lookup"><span data-stu-id="acf34-141">IX</span></span>  <br/> |<span data-ttu-id="acf34-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="acf34-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="acf34-143">opcional</span><span class="sxs-lookup"><span data-stu-id="acf34-143">optional</span></span>  <br/> |<span data-ttu-id="acf34-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="acf34-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="acf34-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="acf34-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="acf34-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="acf34-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="acf34-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="acf34-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="acf34-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="acf34-148">LocalName</span></span>  <br/> |<span data-ttu-id="acf34-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="acf34-149">xsd:string</span></span>  <br/> |<span data-ttu-id="acf34-150">opcional</span><span class="sxs-lookup"><span data-stu-id="acf34-150">optional</span></span>  <br/> |<span data-ttu-id="acf34-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="acf34-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="acf34-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="acf34-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="acf34-153">N</span><span class="sxs-lookup"><span data-stu-id="acf34-153">N</span></span>  <br/> |<span data-ttu-id="acf34-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="acf34-154">xsd:string</span></span>  <br/> |<span data-ttu-id="acf34-155">opcional</span><span class="sxs-lookup"><span data-stu-id="acf34-155">optional</span></span>  <br/> |<span data-ttu-id="acf34-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="acf34-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="acf34-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="acf34-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="acf34-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="acf34-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="acf34-159">T</span><span class="sxs-lookup"><span data-stu-id="acf34-159">T</span></span>  <br/> |<span data-ttu-id="acf34-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="acf34-160">xsd:string</span></span>  <br/> |<span data-ttu-id="acf34-161">opcional</span><span class="sxs-lookup"><span data-stu-id="acf34-161">optional</span></span>  <br/> |<span data-ttu-id="acf34-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="acf34-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="acf34-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="acf34-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="acf34-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="acf34-164">Values of the xsd:string type.</span></span>  <br/> |
   

