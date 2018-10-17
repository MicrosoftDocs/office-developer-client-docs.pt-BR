---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica uma estrutura DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383461"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="9267a-103">Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9267a-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9267a-104">Especifica uma estrutura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="9267a-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9267a-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9267a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9267a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9267a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9267a-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9267a-107">DocumentSheet_Type complexType</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9267a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9267a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9267a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9267a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9267a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9267a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9267a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9267a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9267a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="9267a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9267a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9267a-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9267a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9267a-114">Elements and attributes</span></span>

<span data-ttu-id="9267a-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9267a-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9267a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9267a-116">Parent elements</span></span>

|<span data-ttu-id="9267a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9267a-117">**Element**</span></span>|<span data-ttu-id="9267a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9267a-118">**Type**</span></span>|<span data-ttu-id="9267a-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9267a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9267a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="9267a-120">VisioDocument element</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="9267a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="9267a-121">VisioDocument_Type complexType</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9267a-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="9267a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9267a-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9267a-123">Child elements</span></span>

|<span data-ttu-id="9267a-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9267a-124">**Element**</span></span>|<span data-ttu-id="9267a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9267a-125">**Type**</span></span>|<span data-ttu-id="9267a-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9267a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9267a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="9267a-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="9267a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9267a-128">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9267a-129">Especifica uma célula em uma DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="9267a-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9267a-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9267a-130">Attributes</span></span>

|<span data-ttu-id="9267a-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9267a-131">**Attribute**</span></span>|<span data-ttu-id="9267a-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9267a-132">**Type**</span></span>|<span data-ttu-id="9267a-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9267a-133">**Required**</span></span>|<span data-ttu-id="9267a-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9267a-134">**Description**</span></span>|<span data-ttu-id="9267a-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9267a-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9267a-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="9267a-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="9267a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9267a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9267a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9267a-138">optional</span></span>  <br/> |<span data-ttu-id="9267a-139">Descreve se o nome foi personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9267a-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="9267a-140">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="9267a-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="9267a-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9267a-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9267a-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9267a-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9267a-143">opcional</span><span class="sxs-lookup"><span data-stu-id="9267a-143">optional</span></span>  <br/> |<span data-ttu-id="9267a-144">Descreve se o nome universal foi personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9267a-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="9267a-145">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="9267a-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="9267a-146">Nome</span><span class="sxs-lookup"><span data-stu-id="9267a-146">Name</span></span>  <br/> |<span data-ttu-id="9267a-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9267a-147">xsd:string</span></span>  <br/> |<span data-ttu-id="9267a-148">opcional</span><span class="sxs-lookup"><span data-stu-id="9267a-148">optional</span></span>  <br/> |<span data-ttu-id="9267a-149">Especifica o nome dependente de idioma da DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="9267a-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="9267a-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9267a-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9267a-151">NameU</span><span class="sxs-lookup"><span data-stu-id="9267a-151">NameU Property</span></span>  <br/> |<span data-ttu-id="9267a-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9267a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="9267a-153">opcional</span><span class="sxs-lookup"><span data-stu-id="9267a-153">optional</span></span>  <br/> |<span data-ttu-id="9267a-154">Especifica o nome independente de idioma da DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="9267a-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="9267a-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9267a-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9267a-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="9267a-156">uniqueId</span></span>  <br/> |<span data-ttu-id="9267a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9267a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="9267a-158">opcional</span><span class="sxs-lookup"><span data-stu-id="9267a-158">optional</span></span>  <br/> |<span data-ttu-id="9267a-159">Cadeia de caracteres opcional.</span><span class="sxs-lookup"><span data-stu-id="9267a-159">Optional query string parameters</span></span> <span data-ttu-id="9267a-160">Um GUID (identificador global exclusivo) que identifica a forma.</span><span class="sxs-lookup"><span data-stu-id="9267a-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="9267a-161">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9267a-161">Values of the xsd:string type.</span></span>  <br/> |
   

