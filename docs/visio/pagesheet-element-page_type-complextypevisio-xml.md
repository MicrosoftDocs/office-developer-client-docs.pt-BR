---
title: Elemento PageSheet (Page_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica as propriedades da página de desenho associada à página de desenho.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540620"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="32fcc-103">Elemento PageSheet (Page_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="32fcc-103">PageSheet element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="32fcc-104">Especifica as propriedades da página de desenho associada à página de desenho.</span><span class="sxs-lookup"><span data-stu-id="32fcc-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32fcc-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="32fcc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32fcc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="32fcc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="32fcc-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="32fcc-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="32fcc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="32fcc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="32fcc-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="32fcc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="32fcc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="32fcc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="32fcc-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="32fcc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="32fcc-112">Pages. xml</span><span class="sxs-lookup"><span data-stu-id="32fcc-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32fcc-113">Definição</span><span class="sxs-lookup"><span data-stu-id="32fcc-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32fcc-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="32fcc-114">Elements and attributes</span></span>

<span data-ttu-id="32fcc-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="32fcc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="32fcc-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="32fcc-116">Parent elements</span></span>

|<span data-ttu-id="32fcc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="32fcc-117">**Element**</span></span>|<span data-ttu-id="32fcc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="32fcc-118">**Type**</span></span>|<span data-ttu-id="32fcc-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32fcc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32fcc-120">Page</span><span class="sxs-lookup"><span data-stu-id="32fcc-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32fcc-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="32fcc-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32fcc-122">Contém elementos que definem uma página no documento.</span><span class="sxs-lookup"><span data-stu-id="32fcc-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="32fcc-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="32fcc-123">Child elements</span></span>

<span data-ttu-id="32fcc-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="32fcc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32fcc-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="32fcc-125">Attributes</span></span>

|<span data-ttu-id="32fcc-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="32fcc-126">**Attribute**</span></span>|<span data-ttu-id="32fcc-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="32fcc-127">**Type**</span></span>|<span data-ttu-id="32fcc-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="32fcc-128">**Required**</span></span>|<span data-ttu-id="32fcc-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32fcc-129">**Description**</span></span>|<span data-ttu-id="32fcc-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="32fcc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="32fcc-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="32fcc-131">FillStyle</span></span>  <br/> |<span data-ttu-id="32fcc-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32fcc-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32fcc-133">opcional</span><span class="sxs-lookup"><span data-stu-id="32fcc-133">optional</span></span>  <br/> |<span data-ttu-id="32fcc-134">Especifica a identificação da folha de estilos a partir da qual a formatação de preenchimento será herdada.</span><span class="sxs-lookup"><span data-stu-id="32fcc-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="32fcc-135">DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="32fcc-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="32fcc-136">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32fcc-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32fcc-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="32fcc-137">LineStyle</span></span>  <br/> |<span data-ttu-id="32fcc-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32fcc-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32fcc-139">opcional</span><span class="sxs-lookup"><span data-stu-id="32fcc-139">optional</span></span>  <br/> |<span data-ttu-id="32fcc-140">Especifica a identificação da folha de estilos da qual herdar a formatação de linha.</span><span class="sxs-lookup"><span data-stu-id="32fcc-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="32fcc-141">DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="32fcc-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="32fcc-142">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32fcc-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32fcc-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="32fcc-143">TextStyle</span></span>  <br/> |<span data-ttu-id="32fcc-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32fcc-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32fcc-145">opcional</span><span class="sxs-lookup"><span data-stu-id="32fcc-145">optional</span></span>  <br/> |<span data-ttu-id="32fcc-146">Especifica a identificação da folha de estilos a partir da qual a formatação de texto será herdada.</span><span class="sxs-lookup"><span data-stu-id="32fcc-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="32fcc-147">DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="32fcc-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="32fcc-148">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32fcc-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32fcc-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="32fcc-149">UniqueID</span></span>  <br/> |<span data-ttu-id="32fcc-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="32fcc-150">xsd:string</span></span>  <br/> |<span data-ttu-id="32fcc-151">opcional</span><span class="sxs-lookup"><span data-stu-id="32fcc-151">optional</span></span>  <br/> |<span data-ttu-id="32fcc-152">A identificação exclusiva do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="32fcc-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="32fcc-153">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="32fcc-153">Values of the xsd:string type.</span></span>  <br/> |
   

