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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283483"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="02de5-103">Elemento Row (seção Shape Data) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="02de5-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="02de5-104">Especifica uma entrada de dados de forma para associar dados a uma forma.</span><span class="sxs-lookup"><span data-stu-id="02de5-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02de5-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="02de5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02de5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="02de5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02de5-107">Shape Data_Type</span><span class="sxs-lookup"><span data-stu-id="02de5-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02de5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02de5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02de5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="02de5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02de5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="02de5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02de5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="02de5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02de5-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="02de5-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02de5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="02de5-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02de5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="02de5-114">Elements and attributes</span></span>

<span data-ttu-id="02de5-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="02de5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02de5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="02de5-116">Parent elements</span></span>

|<span data-ttu-id="02de5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02de5-117">**Element**</span></span>|<span data-ttu-id="02de5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02de5-118">**Type**</span></span>|<span data-ttu-id="02de5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02de5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02de5-120">Section</span><span class="sxs-lookup"><span data-stu-id="02de5-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02de5-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="02de5-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02de5-122">Especifica uma entrada de dados de forma para associar dados a uma forma.</span><span class="sxs-lookup"><span data-stu-id="02de5-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02de5-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="02de5-123">Child elements</span></span>

|<span data-ttu-id="02de5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02de5-124">**Element**</span></span>|<span data-ttu-id="02de5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02de5-125">**Type**</span></span>|<span data-ttu-id="02de5-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02de5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02de5-127">Cell</span><span class="sxs-lookup"><span data-stu-id="02de5-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="02de5-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="02de5-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02de5-129">Especifica uma propriedade dos dados de forma.</span><span class="sxs-lookup"><span data-stu-id="02de5-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="02de5-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="02de5-130">Attributes</span></span>

|<span data-ttu-id="02de5-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="02de5-131">**Attribute**</span></span>|<span data-ttu-id="02de5-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02de5-132">**Type**</span></span>|<span data-ttu-id="02de5-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="02de5-133">**Required**</span></span>|<span data-ttu-id="02de5-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02de5-134">**Description**</span></span>|<span data-ttu-id="02de5-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="02de5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02de5-136">Del</span><span class="sxs-lookup"><span data-stu-id="02de5-136">Del</span></span>  <br/> |<span data-ttu-id="02de5-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="02de5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02de5-138">opcional</span><span class="sxs-lookup"><span data-stu-id="02de5-138">optional</span></span>  <br/> |<span data-ttu-id="02de5-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="02de5-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="02de5-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="02de5-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02de5-141">IX</span><span class="sxs-lookup"><span data-stu-id="02de5-141">IX</span></span>  <br/> |<span data-ttu-id="02de5-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02de5-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02de5-143">opcional</span><span class="sxs-lookup"><span data-stu-id="02de5-143">optional</span></span>  <br/> |<span data-ttu-id="02de5-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="02de5-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="02de5-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="02de5-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="02de5-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="02de5-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="02de5-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="02de5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02de5-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="02de5-148">LocalName</span></span>  <br/> |<span data-ttu-id="02de5-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02de5-149">xsd:string</span></span>  <br/> |<span data-ttu-id="02de5-150">opcional</span><span class="sxs-lookup"><span data-stu-id="02de5-150">optional</span></span>  <br/> |<span data-ttu-id="02de5-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="02de5-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="02de5-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02de5-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02de5-153">N</span><span class="sxs-lookup"><span data-stu-id="02de5-153">N</span></span>  <br/> |<span data-ttu-id="02de5-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02de5-154">xsd:string</span></span>  <br/> |<span data-ttu-id="02de5-155">opcional</span><span class="sxs-lookup"><span data-stu-id="02de5-155">optional</span></span>  <br/> |<span data-ttu-id="02de5-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="02de5-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="02de5-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="02de5-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="02de5-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02de5-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02de5-159">T</span><span class="sxs-lookup"><span data-stu-id="02de5-159">T</span></span>  <br/> |<span data-ttu-id="02de5-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02de5-160">xsd:string</span></span>  <br/> |<span data-ttu-id="02de5-161">opcional</span><span class="sxs-lookup"><span data-stu-id="02de5-161">optional</span></span>  <br/> |<span data-ttu-id="02de5-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="02de5-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="02de5-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="02de5-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="02de5-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02de5-164">Values of the xsd:string type.</span></span>  <br/> |
   

