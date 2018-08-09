---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica uma estrutura DocumentSheet.
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771767"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="7ff1d-103">Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7ff1d-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7ff1d-104">Especifica uma estrutura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ff1d-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="7ff1d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ff1d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7ff1d-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="7ff1d-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7ff1d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7ff1d-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7ff1d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7ff1d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7ff1d-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7ff1d-112">Document</span><span class="sxs-lookup"><span data-stu-id="7ff1d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ff1d-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7ff1d-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7ff1d-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7ff1d-114">Elements and attributes</span></span>

<span data-ttu-id="7ff1d-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7ff1d-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7ff1d-116">Parent elements</span></span>

|<span data-ttu-id="7ff1d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-117">**Element**</span></span>|<span data-ttu-id="7ff1d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-118">**Type**</span></span>|<span data-ttu-id="7ff1d-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ff1d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7ff1d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7ff1d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7ff1d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7ff1d-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ff1d-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7ff1d-123">Child elements</span></span>

|<span data-ttu-id="7ff1d-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-124">**Element**</span></span>|<span data-ttu-id="7ff1d-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-125">**Type**</span></span>|<span data-ttu-id="7ff1d-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ff1d-127">Célula</span><span class="sxs-lookup"><span data-stu-id="7ff1d-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="7ff1d-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7ff1d-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7ff1d-129">Especifica uma célula em um DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7ff1d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ff1d-130">Attributes</span></span>

|<span data-ttu-id="7ff1d-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-131">**Attribute**</span></span>|<span data-ttu-id="7ff1d-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-132">**Type**</span></span>|<span data-ttu-id="7ff1d-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-133">**Required**</span></span>|<span data-ttu-id="7ff1d-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-134">**Description**</span></span>|<span data-ttu-id="7ff1d-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7ff1d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7ff1d-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="7ff1d-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="7ff1d-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="7ff1d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7ff1d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7ff1d-138">optional</span></span>  <br/> |<span data-ttu-id="7ff1d-139">Descreve como se o nome tiver sido personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="7ff1d-140">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="7ff1d-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="7ff1d-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="7ff1d-142">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="7ff1d-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7ff1d-143">opcional</span><span class="sxs-lookup"><span data-stu-id="7ff1d-143">optional</span></span>  <br/> |<span data-ttu-id="7ff1d-144">Descreve como se o nome universal foi personalizado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="7ff1d-145">Valores do tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="7ff1d-146">Nome</span><span class="sxs-lookup"><span data-stu-id="7ff1d-146">Name</span></span>  <br/> |<span data-ttu-id="7ff1d-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7ff1d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="7ff1d-148">opcional</span><span class="sxs-lookup"><span data-stu-id="7ff1d-148">optional</span></span>  <br/> |<span data-ttu-id="7ff1d-149">Especifica o nome de dependente de idioma do DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="7ff1d-150">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ff1d-151">NameU</span><span class="sxs-lookup"><span data-stu-id="7ff1d-151">NameU</span></span>  <br/> |<span data-ttu-id="7ff1d-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7ff1d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="7ff1d-153">opcional</span><span class="sxs-lookup"><span data-stu-id="7ff1d-153">optional</span></span>  <br/> |<span data-ttu-id="7ff1d-154">Especifica o nome de independente de idioma do DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="7ff1d-155">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ff1d-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="7ff1d-156">UniqueID</span></span>  <br/> |<span data-ttu-id="7ff1d-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7ff1d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="7ff1d-158">opcional</span><span class="sxs-lookup"><span data-stu-id="7ff1d-158">optional</span></span>  <br/> |<span data-ttu-id="7ff1d-159">Cadeia de caracteres opcional.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-159">Optional string.</span></span> <span data-ttu-id="7ff1d-160">Um GUID (identificador global exclusivo) que identifica a forma.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="7ff1d-161">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7ff1d-161">Values of the xsd:string type.</span></span>  <br/> |
   
