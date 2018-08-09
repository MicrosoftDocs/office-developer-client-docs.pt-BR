---
title: Elemento de linha (seção Shape Data) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica uma entrada de dados de forma para associar os dados uma forma.
ms.openlocfilehash: 19dc4fe4759e7546f56160e41100d73721f9f6e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772786"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="d8366-103">Elemento de linha (seção Shape Data) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d8366-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="d8366-104">Especifica uma entrada de dados de forma para associar os dados uma forma.</span><span class="sxs-lookup"><span data-stu-id="d8366-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8366-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="d8366-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8366-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d8366-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d8366-107">Forma Data_Type</span><span class="sxs-lookup"><span data-stu-id="d8366-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d8366-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8366-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d8366-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8366-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d8366-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d8366-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d8366-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="d8366-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d8366-112"># XML do mestre, página # XML</span><span class="sxs-lookup"><span data-stu-id="d8366-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8366-113">Definição</span><span class="sxs-lookup"><span data-stu-id="d8366-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8366-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d8366-114">Elements and attributes</span></span>

<span data-ttu-id="d8366-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d8366-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d8366-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d8366-116">Parent elements</span></span>

|<span data-ttu-id="d8366-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8366-117">**Element**</span></span>|<span data-ttu-id="d8366-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8366-118">**Type**</span></span>|<span data-ttu-id="d8366-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8366-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8366-120">Seção</span><span class="sxs-lookup"><span data-stu-id="d8366-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8366-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d8366-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8366-122">Especifica uma entrada de dados de forma para associar os dados uma forma.</span><span class="sxs-lookup"><span data-stu-id="d8366-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8366-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8366-123">Child elements</span></span>

|<span data-ttu-id="d8366-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8366-124">**Element**</span></span>|<span data-ttu-id="d8366-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8366-125">**Type**</span></span>|<span data-ttu-id="d8366-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8366-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8366-127">Célula</span><span class="sxs-lookup"><span data-stu-id="d8366-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d8366-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d8366-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8366-129">Especifica uma propriedade dos dados da forma.</span><span class="sxs-lookup"><span data-stu-id="d8366-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d8366-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8366-130">Attributes</span></span>

|<span data-ttu-id="d8366-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8366-131">**Attribute**</span></span>|<span data-ttu-id="d8366-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8366-132">**Type**</span></span>|<span data-ttu-id="d8366-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d8366-133">**Required**</span></span>|<span data-ttu-id="d8366-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8366-134">**Description**</span></span>|<span data-ttu-id="d8366-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d8366-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8366-136">DEL</span><span class="sxs-lookup"><span data-stu-id="d8366-136">Del</span></span>  <br/> |<span data-ttu-id="d8366-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d8366-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8366-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d8366-138">optional</span></span>  <br/> |<span data-ttu-id="d8366-139">Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="d8366-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="d8366-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8366-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d8366-141">IX</span><span class="sxs-lookup"><span data-stu-id="d8366-141">IX</span></span>  <br/> |<span data-ttu-id="d8366-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8366-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8366-143">opcional</span><span class="sxs-lookup"><span data-stu-id="d8366-143">optional</span></span>  <br/> |<span data-ttu-id="d8366-144">Especifica o identificador baseada em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="d8366-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="d8366-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias.</span><span class="sxs-lookup"><span data-stu-id="d8366-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="d8366-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="d8366-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d8366-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8366-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8366-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="d8366-148">LocalName</span></span>  <br/> |<span data-ttu-id="d8366-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8366-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d8366-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d8366-150">optional</span></span>  <br/> |<span data-ttu-id="d8366-151">Especifica o nome exclusivo do dependentes de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="d8366-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="d8366-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8366-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8366-153">N</span><span class="sxs-lookup"><span data-stu-id="d8366-153">N</span></span>  <br/> |<span data-ttu-id="d8366-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8366-154">xsd:string</span></span>  <br/> |<span data-ttu-id="d8366-155">opcional</span><span class="sxs-lookup"><span data-stu-id="d8366-155">optional</span></span>  <br/> |<span data-ttu-id="d8366-156">Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="d8366-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="d8366-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="d8366-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d8366-158">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8366-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8366-159">T</span><span class="sxs-lookup"><span data-stu-id="d8366-159">T</span></span>  <br/> |<span data-ttu-id="d8366-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d8366-160">xsd:string</span></span>  <br/> |<span data-ttu-id="d8366-161">opcional</span><span class="sxs-lookup"><span data-stu-id="d8366-161">optional</span></span>  <br/> |<span data-ttu-id="d8366-162">Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="d8366-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="d8366-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="d8366-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="d8366-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d8366-164">Values of the xsd:string type.</span></span>  <br/> |
   

