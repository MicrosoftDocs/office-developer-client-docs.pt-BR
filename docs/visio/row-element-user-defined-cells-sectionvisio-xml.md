---
title: Elemento Row (Seção User-defined Cells) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538169"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="062ae-103">Elemento Row (Seção User-defined Cells) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="062ae-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="062ae-104">Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="062ae-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="062ae-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="062ae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="062ae-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="062ae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="062ae-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="062ae-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="062ae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="062ae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="062ae-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="062ae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="062ae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="062ae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="062ae-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="062ae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="062ae-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="062ae-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="062ae-113">Definição</span><span class="sxs-lookup"><span data-stu-id="062ae-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="062ae-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="062ae-114">Elements and attributes</span></span>

<span data-ttu-id="062ae-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="062ae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="062ae-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="062ae-116">Parent elements</span></span>

|<span data-ttu-id="062ae-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="062ae-117">**Element**</span></span>|<span data-ttu-id="062ae-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="062ae-118">**Type**</span></span>|<span data-ttu-id="062ae-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="062ae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="062ae-120">Section</span><span class="sxs-lookup"><span data-stu-id="062ae-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="062ae-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="062ae-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="062ae-122">Uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="062ae-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="062ae-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="062ae-123">Child elements</span></span>

|<span data-ttu-id="062ae-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="062ae-124">**Element**</span></span>|<span data-ttu-id="062ae-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="062ae-125">**Type**</span></span>|<span data-ttu-id="062ae-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="062ae-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="062ae-127">Cell</span><span class="sxs-lookup"><span data-stu-id="062ae-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="062ae-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="062ae-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="062ae-129">Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.</span><span class="sxs-lookup"><span data-stu-id="062ae-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="062ae-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="062ae-130">Attributes</span></span>

|<span data-ttu-id="062ae-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="062ae-131">**Attribute**</span></span>|<span data-ttu-id="062ae-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="062ae-132">**Type**</span></span>|<span data-ttu-id="062ae-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="062ae-133">**Required**</span></span>|<span data-ttu-id="062ae-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="062ae-134">**Description**</span></span>|<span data-ttu-id="062ae-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="062ae-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="062ae-136">Del</span><span class="sxs-lookup"><span data-stu-id="062ae-136">Del</span></span>  <br/> |<span data-ttu-id="062ae-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="062ae-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="062ae-138">opcional</span><span class="sxs-lookup"><span data-stu-id="062ae-138">optional</span></span>  <br/> |<span data-ttu-id="062ae-139">Especifica se uma linha que seria herdada de uma forma mestra foi excluída.</span><span class="sxs-lookup"><span data-stu-id="062ae-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="062ae-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="062ae-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="062ae-141">IX</span><span class="sxs-lookup"><span data-stu-id="062ae-141">IX</span></span>  <br/> |<span data-ttu-id="062ae-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="062ae-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="062ae-143">opcional</span><span class="sxs-lookup"><span data-stu-id="062ae-143">optional</span></span>  <br/> |<span data-ttu-id="062ae-144">Especifica o identificador baseado em um para a linha.</span><span class="sxs-lookup"><span data-stu-id="062ae-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="062ae-145">Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs.</span><span class="sxs-lookup"><span data-stu-id="062ae-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="062ae-146">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="062ae-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="062ae-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="062ae-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="062ae-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="062ae-148">LocalName</span></span>  <br/> |<span data-ttu-id="062ae-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="062ae-149">xsd:string</span></span>  <br/> |<span data-ttu-id="062ae-150">opcional</span><span class="sxs-lookup"><span data-stu-id="062ae-150">optional</span></span>  <br/> |<span data-ttu-id="062ae-151">Especifica o nome exclusivo dependente de idioma da linha.</span><span class="sxs-lookup"><span data-stu-id="062ae-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="062ae-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="062ae-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="062ae-153">N</span><span class="sxs-lookup"><span data-stu-id="062ae-153">N</span></span>  <br/> |<span data-ttu-id="062ae-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="062ae-154">xsd:string</span></span>  <br/> |<span data-ttu-id="062ae-155">opcional</span><span class="sxs-lookup"><span data-stu-id="062ae-155">optional</span></span>  <br/> |<span data-ttu-id="062ae-156">Especifica o nome exclusivo independente do idioma da linha. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag.</span><span class="sxs-lookup"><span data-stu-id="062ae-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="062ae-157">Uma linha só pode ter um dos atributos IX ou N.</span><span class="sxs-lookup"><span data-stu-id="062ae-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="062ae-158">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="062ae-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="062ae-159">T</span><span class="sxs-lookup"><span data-stu-id="062ae-159">T</span></span>  <br/> |<span data-ttu-id="062ae-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="062ae-160">xsd:string</span></span>  <br/> |<span data-ttu-id="062ae-161">opcional</span><span class="sxs-lookup"><span data-stu-id="062ae-161">optional</span></span>  <br/> |<span data-ttu-id="062ae-162">Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria.</span><span class="sxs-lookup"><span data-stu-id="062ae-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="062ae-163">O atributo T só é usado para a seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="062ae-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="062ae-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="062ae-164">Values of the xsd:string type.</span></span>  <br/> |
   

