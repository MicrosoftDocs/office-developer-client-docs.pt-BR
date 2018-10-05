---
title: Elemento PageSheet (Page_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica as propriedades da página de desenho associado à página de desenho.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395130"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="39918-103">Elemento PageSheet (Page_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="39918-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="39918-104">Especifica as propriedades da página de desenho associado à página de desenho.</span><span class="sxs-lookup"><span data-stu-id="39918-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39918-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="39918-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39918-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="39918-106">**Element type**</span></span> <br/> |[<span data-ttu-id="39918-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="39918-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="39918-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="39918-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="39918-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="39918-109">**Schema file**</span></span> <br/> |<span data-ttu-id="39918-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="39918-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="39918-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="39918-111">**Document parts**</span></span> <br/> |<span data-ttu-id="39918-112">Pages.XML</span><span class="sxs-lookup"><span data-stu-id="39918-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39918-113">Definição</span><span class="sxs-lookup"><span data-stu-id="39918-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39918-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="39918-114">Elements and attributes</span></span>

<span data-ttu-id="39918-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="39918-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="39918-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="39918-116">Parent elements</span></span>

|<span data-ttu-id="39918-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="39918-117">**Element**</span></span>|<span data-ttu-id="39918-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39918-118">**Type**</span></span>|<span data-ttu-id="39918-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39918-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39918-120">Page</span><span class="sxs-lookup"><span data-stu-id="39918-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="39918-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="39918-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39918-122">Contém os elementos que definem uma página do documento.</span><span class="sxs-lookup"><span data-stu-id="39918-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39918-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="39918-123">Child elements</span></span>

<span data-ttu-id="39918-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="39918-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39918-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="39918-125">Attributes</span></span>

|<span data-ttu-id="39918-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="39918-126">**Attribute**</span></span>|<span data-ttu-id="39918-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39918-127">**Type**</span></span>|<span data-ttu-id="39918-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="39918-128">**Required**</span></span>|<span data-ttu-id="39918-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39918-129">**Description**</span></span>|<span data-ttu-id="39918-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="39918-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39918-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="39918-131">FillStyle</span></span>  <br/> |<span data-ttu-id="39918-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="39918-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="39918-133">opcional</span><span class="sxs-lookup"><span data-stu-id="39918-133">optional</span></span>  <br/> |<span data-ttu-id="39918-134">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="39918-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="39918-135">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="39918-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="39918-136">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="39918-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="39918-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="39918-137">LineStyle</span></span>  <br/> |<span data-ttu-id="39918-138">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="39918-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="39918-139">opcional</span><span class="sxs-lookup"><span data-stu-id="39918-139">optional</span></span>  <br/> |<span data-ttu-id="39918-140">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de linha.</span><span class="sxs-lookup"><span data-stu-id="39918-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="39918-141">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="39918-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="39918-142">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="39918-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="39918-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="39918-143">TextStyle</span></span>  <br/> |<span data-ttu-id="39918-144">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="39918-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="39918-145">opcional</span><span class="sxs-lookup"><span data-stu-id="39918-145">optional</span></span>  <br/> |<span data-ttu-id="39918-146">Especifica a ID da folha de estilos a partir dos quais herdam a formatação de texto.</span><span class="sxs-lookup"><span data-stu-id="39918-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="39918-147">Ela deve ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="39918-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="39918-148">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="39918-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="39918-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="39918-149">UniqueID</span></span>  <br/> |<span data-ttu-id="39918-150">XSD: String</span><span class="sxs-lookup"><span data-stu-id="39918-150">xsd:string</span></span>  <br/> |<span data-ttu-id="39918-151">opcional</span><span class="sxs-lookup"><span data-stu-id="39918-151">optional</span></span>  <br/> |<span data-ttu-id="39918-152">A ID exclusiva do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="39918-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="39918-153">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="39918-153">Values of the xsd:string type.</span></span>  <br/> |
   

