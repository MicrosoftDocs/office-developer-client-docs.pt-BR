---
title: Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica as propriedades usadas para identificar o autor de um comentário em um desenho.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771281"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="1a87d-103">Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1a87d-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1a87d-104">Especifica as propriedades usadas para identificar o autor de um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="1a87d-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a87d-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="1a87d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a87d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1a87d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1a87d-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1a87d-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1a87d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1a87d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1a87d-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1a87d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1a87d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1a87d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1a87d-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1a87d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1a87d-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="1a87d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a87d-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1a87d-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1a87d-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1a87d-114">Elements and attributes</span></span>

<span data-ttu-id="1a87d-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1a87d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1a87d-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1a87d-116">Parent elements</span></span>

|<span data-ttu-id="1a87d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a87d-117">**Element**</span></span>|<span data-ttu-id="1a87d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1a87d-118">**Type**</span></span>|<span data-ttu-id="1a87d-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a87d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a87d-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="1a87d-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1a87d-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="1a87d-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1a87d-122">Especifica os autores em um desenho.</span><span class="sxs-lookup"><span data-stu-id="1a87d-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1a87d-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1a87d-123">Child elements</span></span>

<span data-ttu-id="1a87d-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1a87d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a87d-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a87d-125">Attributes</span></span>

|<span data-ttu-id="1a87d-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1a87d-126">**Attribute**</span></span>|<span data-ttu-id="1a87d-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1a87d-127">**Type**</span></span>|<span data-ttu-id="1a87d-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1a87d-128">**Required**</span></span>|<span data-ttu-id="1a87d-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a87d-129">**Description**</span></span>|<span data-ttu-id="1a87d-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1a87d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1a87d-131">ID</span><span class="sxs-lookup"><span data-stu-id="1a87d-131">ID</span></span>  <br/> |<span data-ttu-id="1a87d-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1a87d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1a87d-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1a87d-133">required</span></span>  <br/> |<span data-ttu-id="1a87d-134">Um valor baseado em um que identifica o autor.</span><span class="sxs-lookup"><span data-stu-id="1a87d-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="1a87d-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1a87d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1a87d-136">Initials</span><span class="sxs-lookup"><span data-stu-id="1a87d-136">Initials</span></span>  <br/> |<span data-ttu-id="1a87d-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1a87d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1a87d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1a87d-138">optional</span></span>  <br/> |<span data-ttu-id="1a87d-139">As iniciais do autor.</span><span class="sxs-lookup"><span data-stu-id="1a87d-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="1a87d-140">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1a87d-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a87d-141">Nome</span><span class="sxs-lookup"><span data-stu-id="1a87d-141">Name</span></span>  <br/> |<span data-ttu-id="1a87d-142">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1a87d-142">xsd:string</span></span>  <br/> |<span data-ttu-id="1a87d-143">opcional</span><span class="sxs-lookup"><span data-stu-id="1a87d-143">optional</span></span>  <br/> |<span data-ttu-id="1a87d-144">O nome do autor.</span><span class="sxs-lookup"><span data-stu-id="1a87d-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="1a87d-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1a87d-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a87d-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="1a87d-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="1a87d-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1a87d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="1a87d-148">opcional</span><span class="sxs-lookup"><span data-stu-id="1a87d-148">optional</span></span>  <br/> |<span data-ttu-id="1a87d-149">Um identificador exclusivo para o autor.</span><span class="sxs-lookup"><span data-stu-id="1a87d-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="1a87d-150">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1a87d-150">Values of the xsd:string type.</span></span>  <br/> |
   

