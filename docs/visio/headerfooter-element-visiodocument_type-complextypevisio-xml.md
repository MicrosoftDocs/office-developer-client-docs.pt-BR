---
title: Elemento HeaderFooter (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contém elementos do cabeçalho e rodapé de um documento.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319020"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="3341c-103">Elemento HeaderFooter (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3341c-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3341c-104">Contém elementos do cabeçalho e rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3341c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="3341c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3341c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3341c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3341c-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3341c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3341c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3341c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3341c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3341c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3341c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3341c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="3341c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3341c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="3341c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3341c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="3341c-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3341c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3341c-114">Elements and attributes</span></span>

<span data-ttu-id="3341c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3341c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3341c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3341c-116">Parent elements</span></span>

|<span data-ttu-id="3341c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3341c-117">**Element**</span></span>|<span data-ttu-id="3341c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3341c-118">**Type**</span></span>|<span data-ttu-id="3341c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3341c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3341c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3341c-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3341c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3341c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3341c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3341c-123">Child elements</span></span>

|<span data-ttu-id="3341c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3341c-124">**Element**</span></span>|<span data-ttu-id="3341c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3341c-125">**Type**</span></span>|<span data-ttu-id="3341c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3341c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3341c-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="3341c-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-129">Contém a cadeia de caracteres de texto que aparece na parte central do rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="3341c-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="3341c-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-132">Contém a cadeia de caracteres de texto que aparece na parte esquerda do rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="3341c-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="3341c-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-135">Especifica a margem do rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="3341c-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="3341c-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-138">Contém a cadeia de caracteres de texto que aparece na parte direita do rodapé de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="3341c-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="3341c-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-141">Obtém ou define a sequência de caracteres de texto que é exibida na parte central do cabeçalho de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="3341c-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="3341c-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-144">Especifica a fonte utilizada no texto do cabeçalho e do rodapé.</span><span class="sxs-lookup"><span data-stu-id="3341c-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="3341c-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="3341c-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-147">Contém a cadeia de caracteres de texto que aparece na parte esquerda do cabeçalho de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="3341c-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="3341c-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-150">Especifica a margem do cabeçalho de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="3341c-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="3341c-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3341c-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="3341c-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3341c-153">Contém a cadeia de caracteres de texto que aparece na parte direita do cabeçalho de um documento.</span><span class="sxs-lookup"><span data-stu-id="3341c-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3341c-154">Atributos</span><span class="sxs-lookup"><span data-stu-id="3341c-154">Attributes</span></span>

|<span data-ttu-id="3341c-155">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3341c-155">**Attribute**</span></span>|<span data-ttu-id="3341c-156">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3341c-156">**Type**</span></span>|<span data-ttu-id="3341c-157">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3341c-157">**Required**</span></span>|<span data-ttu-id="3341c-158">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3341c-158">**Description**</span></span>|<span data-ttu-id="3341c-159">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3341c-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3341c-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="3341c-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="3341c-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3341c-161">xsd:string</span></span>  <br/> |<span data-ttu-id="3341c-162">opcional</span><span class="sxs-lookup"><span data-stu-id="3341c-162">optional</span></span>  <br/> |<span data-ttu-id="3341c-163">O valor RGB da cor do texto do cabeçalho e rodapé em notação hexadecimal; por exemplo, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="3341c-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="3341c-164">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3341c-164">Values of the xsd:string type.</span></span>  <br/> |
   

