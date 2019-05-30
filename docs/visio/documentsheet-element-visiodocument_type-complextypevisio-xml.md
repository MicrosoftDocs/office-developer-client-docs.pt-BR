---
title: Elemento DocumentSheet (VisioDocument_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica uma estrutura DocumentSheet.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540039"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="62d5a-103">Elemento DocumentSheet (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="62d5a-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="62d5a-104">Especifica uma estrutura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="62d5a-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62d5a-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="62d5a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62d5a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="62d5a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62d5a-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="62d5a-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62d5a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62d5a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62d5a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="62d5a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62d5a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62d5a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62d5a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="62d5a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62d5a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="62d5a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62d5a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="62d5a-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62d5a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="62d5a-114">Elements and attributes</span></span>

<span data-ttu-id="62d5a-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="62d5a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62d5a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="62d5a-116">Parent elements</span></span>

|<span data-ttu-id="62d5a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62d5a-117">**Element**</span></span>|<span data-ttu-id="62d5a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62d5a-118">**Type**</span></span>|<span data-ttu-id="62d5a-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62d5a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62d5a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="62d5a-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="62d5a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="62d5a-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62d5a-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="62d5a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62d5a-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="62d5a-123">Child elements</span></span>

|<span data-ttu-id="62d5a-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62d5a-124">**Element**</span></span>|<span data-ttu-id="62d5a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62d5a-125">**Type**</span></span>|<span data-ttu-id="62d5a-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62d5a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62d5a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="62d5a-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="62d5a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="62d5a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62d5a-129">Especifica uma célula em uma DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="62d5a-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="62d5a-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="62d5a-130">Attributes</span></span>

|<span data-ttu-id="62d5a-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="62d5a-131">**Attribute**</span></span>|<span data-ttu-id="62d5a-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62d5a-132">**Type**</span></span>|<span data-ttu-id="62d5a-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="62d5a-133">**Required**</span></span>|<span data-ttu-id="62d5a-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62d5a-134">**Description**</span></span>|<span data-ttu-id="62d5a-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="62d5a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62d5a-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="62d5a-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="62d5a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="62d5a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62d5a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="62d5a-138">optional</span></span>  <br/> |<span data-ttu-id="62d5a-139">Descreve se o nome foi personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="62d5a-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="62d5a-140">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="62d5a-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="62d5a-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="62d5a-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="62d5a-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="62d5a-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62d5a-143">opcional</span><span class="sxs-lookup"><span data-stu-id="62d5a-143">optional</span></span>  <br/> |<span data-ttu-id="62d5a-144">Descreve se o nome universal foi personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="62d5a-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="62d5a-145">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="62d5a-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="62d5a-146">Nome</span><span class="sxs-lookup"><span data-stu-id="62d5a-146">Name</span></span>  <br/> |<span data-ttu-id="62d5a-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62d5a-147">xsd:string</span></span>  <br/> |<span data-ttu-id="62d5a-148">opcional</span><span class="sxs-lookup"><span data-stu-id="62d5a-148">optional</span></span>  <br/> |<span data-ttu-id="62d5a-149">Especifica o nome dependente de idioma da DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="62d5a-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="62d5a-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="62d5a-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62d5a-151">NameU</span><span class="sxs-lookup"><span data-stu-id="62d5a-151">NameU</span></span>  <br/> |<span data-ttu-id="62d5a-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62d5a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="62d5a-153">opcional</span><span class="sxs-lookup"><span data-stu-id="62d5a-153">optional</span></span>  <br/> |<span data-ttu-id="62d5a-154">Especifica o nome independente de idioma da DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="62d5a-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="62d5a-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="62d5a-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62d5a-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="62d5a-156">UniqueID</span></span>  <br/> |<span data-ttu-id="62d5a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62d5a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="62d5a-158">opcional</span><span class="sxs-lookup"><span data-stu-id="62d5a-158">optional</span></span>  <br/> |<span data-ttu-id="62d5a-159">Cadeia de caracteres opcional.</span><span class="sxs-lookup"><span data-stu-id="62d5a-159">Optional string.</span></span> <span data-ttu-id="62d5a-160">Um GUID (identificador global exclusivo) que identifica a forma.</span><span class="sxs-lookup"><span data-stu-id="62d5a-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="62d5a-161">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="62d5a-161">Values of the xsd:string type.</span></span>  <br/> |
   

