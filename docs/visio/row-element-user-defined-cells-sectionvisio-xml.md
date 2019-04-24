---
title: Elemento Row (seção User-defined Cells) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas complementares.
ms.openlocfilehash: 8852c1db31e9a9b8f0860c111da32de6d44dc7f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332484"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="7c938-103">Elemento Row (seção User-defined Cells) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7c938-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="7c938-104">Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas complementares.</span><span class="sxs-lookup"><span data-stu-id="7c938-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c938-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="7c938-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c938-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7c938-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7c938-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="7c938-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c938-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c938-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c938-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7c938-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7c938-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7c938-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c938-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7c938-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7c938-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="7c938-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c938-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7c938-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c938-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7c938-114">Elements and attributes</span></span>

<span data-ttu-id="7c938-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7c938-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c938-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7c938-116">Parent elements</span></span>

|<span data-ttu-id="7c938-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7c938-117">**Element**</span></span>|<span data-ttu-id="7c938-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c938-118">**Type**</span></span>|<span data-ttu-id="7c938-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c938-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c938-120">Section</span><span class="sxs-lookup"><span data-stu-id="7c938-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c938-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7c938-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c938-122">Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas complementares.</span><span class="sxs-lookup"><span data-stu-id="7c938-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7c938-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7c938-123">Child elements</span></span>

|<span data-ttu-id="7c938-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7c938-124">**Element**</span></span>|<span data-ttu-id="7c938-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c938-125">**Type**</span></span>|<span data-ttu-id="7c938-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c938-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c938-127">Cell</span><span class="sxs-lookup"><span data-stu-id="7c938-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7c938-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7c938-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c938-129">Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="7c938-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7c938-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c938-130">Attributes</span></span>

|<span data-ttu-id="7c938-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7c938-131">**Attribute**</span></span>|<span data-ttu-id="7c938-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c938-132">**Type**</span></span>|<span data-ttu-id="7c938-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7c938-133">**Required**</span></span>|<span data-ttu-id="7c938-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c938-134">**Description**</span></span>|<span data-ttu-id="7c938-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7c938-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c938-136">Del</span><span class="sxs-lookup"><span data-stu-id="7c938-136">Del</span></span>  <br/> |<span data-ttu-id="7c938-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7c938-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c938-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7c938-138">optional</span></span>  <br/> |<span data-ttu-id="7c938-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="7c938-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="7c938-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7c938-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c938-141">IX</span><span class="sxs-lookup"><span data-stu-id="7c938-141">IX</span></span>  <br/> |<span data-ttu-id="7c938-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c938-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c938-143">opcional</span><span class="sxs-lookup"><span data-stu-id="7c938-143">optional</span></span>  <br/> |<span data-ttu-id="7c938-144">Especifica o identificador baseado em um da linha.</span><span class="sxs-lookup"><span data-stu-id="7c938-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="7c938-145">Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias.</span><span class="sxs-lookup"><span data-stu-id="7c938-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="7c938-146">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7c938-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7c938-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c938-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c938-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="7c938-148">LocalName</span></span>  <br/> |<span data-ttu-id="7c938-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7c938-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7c938-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7c938-150">optional</span></span>  <br/> |<span data-ttu-id="7c938-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="7c938-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="7c938-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7c938-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c938-153">N</span><span class="sxs-lookup"><span data-stu-id="7c938-153">N</span></span>  <br/> |<span data-ttu-id="7c938-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7c938-154">xsd:string</span></span>  <br/> |<span data-ttu-id="7c938-155">opcional</span><span class="sxs-lookup"><span data-stu-id="7c938-155">optional</span></span>  <br/> |<span data-ttu-id="7c938-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="7c938-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="7c938-157">Uma linha pode ter apenas um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="7c938-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7c938-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7c938-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c938-159">T</span><span class="sxs-lookup"><span data-stu-id="7c938-159">T</span></span>  <br/> |<span data-ttu-id="7c938-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7c938-160">xsd:string</span></span>  <br/> |<span data-ttu-id="7c938-161">opcional</span><span class="sxs-lookup"><span data-stu-id="7c938-161">optional</span></span>  <br/> |<span data-ttu-id="7c938-162">Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="7c938-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="7c938-163">O atributo T é usado apenas para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="7c938-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="7c938-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7c938-164">Values of the xsd:string type.</span></span>  <br/> |
   

