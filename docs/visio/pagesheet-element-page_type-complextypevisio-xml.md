---
title: Elemento PageSheet (Page_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica as propriedades da página de desenho associado à página de desenho.
ms.openlocfilehash: ef926af0238b1a44bbaa5c2eae9c0f7c90dc0c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772460"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="631cf-103">Elemento PageSheet (Page_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="631cf-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="631cf-104">Especifica as propriedades da página de desenho associado à página de desenho.</span><span class="sxs-lookup"><span data-stu-id="631cf-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="631cf-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="631cf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="631cf-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="631cf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="631cf-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="631cf-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="631cf-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="631cf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="631cf-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="631cf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="631cf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="631cf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="631cf-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="631cf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="631cf-112">Pages.XML</span><span class="sxs-lookup"><span data-stu-id="631cf-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="631cf-113">Definição</span><span class="sxs-lookup"><span data-stu-id="631cf-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="631cf-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="631cf-114">Elements and attributes</span></span>

<span data-ttu-id="631cf-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="631cf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="631cf-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="631cf-116">Parent elements</span></span>

|<span data-ttu-id="631cf-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="631cf-117">**Element**</span></span>|<span data-ttu-id="631cf-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="631cf-118">**Type**</span></span>|<span data-ttu-id="631cf-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="631cf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="631cf-120">Page</span><span class="sxs-lookup"><span data-stu-id="631cf-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="631cf-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="631cf-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="631cf-122">Contém os elementos que definem uma página do documento.</span><span class="sxs-lookup"><span data-stu-id="631cf-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="631cf-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="631cf-123">Child elements</span></span>

<span data-ttu-id="631cf-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="631cf-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="631cf-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="631cf-125">Attributes</span></span>

|<span data-ttu-id="631cf-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="631cf-126">**Attribute**</span></span>|<span data-ttu-id="631cf-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="631cf-127">**Type**</span></span>|<span data-ttu-id="631cf-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="631cf-128">**Required**</span></span>|<span data-ttu-id="631cf-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="631cf-129">**Description**</span></span>|<span data-ttu-id="631cf-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="631cf-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="631cf-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="631cf-131">FillStyle</span></span>  <br/> |<span data-ttu-id="631cf-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="631cf-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="631cf-133">opcional</span><span class="sxs-lookup"><span data-stu-id="631cf-133">optional</span></span>  <br/> |<span data-ttu-id="631cf-134">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="631cf-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="631cf-135">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="631cf-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="631cf-136">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="631cf-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="631cf-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="631cf-137">LineStyle</span></span>  <br/> |<span data-ttu-id="631cf-138">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="631cf-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="631cf-139">opcional</span><span class="sxs-lookup"><span data-stu-id="631cf-139">optional</span></span>  <br/> |<span data-ttu-id="631cf-140">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de linha.</span><span class="sxs-lookup"><span data-stu-id="631cf-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="631cf-141">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="631cf-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="631cf-142">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="631cf-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="631cf-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="631cf-143">TextStyle</span></span>  <br/> |<span data-ttu-id="631cf-144">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="631cf-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="631cf-145">opcional</span><span class="sxs-lookup"><span data-stu-id="631cf-145">optional</span></span>  <br/> |<span data-ttu-id="631cf-146">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de texto.</span><span class="sxs-lookup"><span data-stu-id="631cf-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="631cf-147">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="631cf-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="631cf-148">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="631cf-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="631cf-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="631cf-149">UniqueID</span></span>  <br/> |<span data-ttu-id="631cf-150">XSD: String</span><span class="sxs-lookup"><span data-stu-id="631cf-150">xsd:string</span></span>  <br/> |<span data-ttu-id="631cf-151">opcional</span><span class="sxs-lookup"><span data-stu-id="631cf-151">optional</span></span>  <br/> |<span data-ttu-id="631cf-152">A ID exclusiva do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="631cf-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="631cf-153">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="631cf-153">Values of the xsd:string type.</span></span>  <br/> |
   

