---
title: Elemento Row (seção Shape Data) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Especifica uma entrada de dados de forma para associar dados a uma forma.
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: 9716521f7bcd531f93be9855ae7835be20cdd0e2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2019
ms.locfileid: "32283483"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="2d350-103">Elemento Row (seção Shape Data) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2d350-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="2d350-104">Especifica uma entrada de dados de forma para associar dados a uma forma.</span><span class="sxs-lookup"><span data-stu-id="2d350-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d350-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="2d350-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d350-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2d350-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2d350-107">Shape Data_Type</span><span class="sxs-lookup"><span data-stu-id="2d350-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2d350-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2d350-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2d350-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d350-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2d350-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2d350-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2d350-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="2d350-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2d350-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="2d350-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2d350-113">Definição</span><span class="sxs-lookup"><span data-stu-id="2d350-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2d350-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2d350-114">Elements and attributes</span></span>

<span data-ttu-id="2d350-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2d350-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2d350-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2d350-116">Parent elements</span></span>

|<span data-ttu-id="2d350-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2d350-117">**Element**</span></span>|<span data-ttu-id="2d350-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d350-118">**Type**</span></span>|<span data-ttu-id="2d350-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d350-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2d350-120">Section</span><span class="sxs-lookup"><span data-stu-id="2d350-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2d350-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2d350-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2d350-122">Especifica uma entrada de dados de forma para associar dados a uma forma.</span><span class="sxs-lookup"><span data-stu-id="2d350-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2d350-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2d350-123">Child elements</span></span>

|<span data-ttu-id="2d350-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2d350-124">**Element**</span></span>|<span data-ttu-id="2d350-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d350-125">**Type**</span></span>|<span data-ttu-id="2d350-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d350-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2d350-127">Cell</span><span class="sxs-lookup"><span data-stu-id="2d350-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2d350-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2d350-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2d350-129">Especifica uma propriedade dos dados de forma.</span><span class="sxs-lookup"><span data-stu-id="2d350-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2d350-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d350-130">Attributes</span></span>

|<span data-ttu-id="2d350-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2d350-131">**Attribute**</span></span>|<span data-ttu-id="2d350-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d350-132">**Type**</span></span>|<span data-ttu-id="2d350-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2d350-133">**Required**</span></span>|<span data-ttu-id="2d350-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d350-134">**Description**</span></span>|<span data-ttu-id="2d350-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2d350-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2d350-136">Del</span><span class="sxs-lookup"><span data-stu-id="2d350-136">Del</span></span>  <br/> |<span data-ttu-id="2d350-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2d350-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2d350-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2d350-138">optional</span></span>  <br/> |<span data-ttu-id="2d350-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="2d350-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="2d350-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2d350-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2d350-141">IX</span><span class="sxs-lookup"><span data-stu-id="2d350-141">IX</span></span>  <br/> |<span data-ttu-id="2d350-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2d350-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2d350-143">opcional</span><span class="sxs-lookup"><span data-stu-id="2d350-143">optional</span></span>  <br/> |<span data-ttu-id="2d350-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="2d350-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="2d350-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="2d350-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="2d350-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="2d350-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2d350-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2d350-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2d350-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="2d350-148">LocalName</span></span>  <br/> |<span data-ttu-id="2d350-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d350-149">xsd:string</span></span>  <br/> |<span data-ttu-id="2d350-150">opcional</span><span class="sxs-lookup"><span data-stu-id="2d350-150">optional</span></span>  <br/> |<span data-ttu-id="2d350-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="2d350-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="2d350-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d350-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d350-153">N</span><span class="sxs-lookup"><span data-stu-id="2d350-153">N</span></span>  <br/> |<span data-ttu-id="2d350-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d350-154">xsd:string</span></span>  <br/> |<span data-ttu-id="2d350-155">opcional</span><span class="sxs-lookup"><span data-stu-id="2d350-155">optional</span></span>  <br/> |<span data-ttu-id="2d350-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="2d350-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="2d350-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="2d350-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2d350-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d350-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d350-159">T</span><span class="sxs-lookup"><span data-stu-id="2d350-159">T</span></span>  <br/> |<span data-ttu-id="2d350-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d350-160">xsd:string</span></span>  <br/> |<span data-ttu-id="2d350-161">opcional</span><span class="sxs-lookup"><span data-stu-id="2d350-161">optional</span></span>  <br/> |<span data-ttu-id="2d350-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="2d350-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="2d350-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="2d350-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="2d350-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d350-164">Values of the xsd:string type.</span></span>  <br/> |
   

