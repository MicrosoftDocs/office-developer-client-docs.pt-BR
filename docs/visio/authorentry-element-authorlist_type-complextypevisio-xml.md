---
title: Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica propriedades usadas para identificar o autor de um comentário em um desenho.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338623"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="a3276-103">Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a3276-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a3276-104">Especifica propriedades usadas para identificar o autor de um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="a3276-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3276-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="a3276-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3276-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a3276-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a3276-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="a3276-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3276-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a3276-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3276-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a3276-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a3276-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a3276-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3276-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="a3276-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a3276-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="a3276-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3276-113">Definição</span><span class="sxs-lookup"><span data-stu-id="a3276-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3276-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a3276-114">Elements and attributes</span></span>

<span data-ttu-id="a3276-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a3276-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3276-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a3276-116">Parent elements</span></span>

|<span data-ttu-id="a3276-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3276-117">**Element**</span></span>|<span data-ttu-id="a3276-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a3276-118">**Type**</span></span>|<span data-ttu-id="a3276-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a3276-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3276-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="a3276-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3276-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="a3276-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3276-122">Especifica os autores em um desenho.</span><span class="sxs-lookup"><span data-stu-id="a3276-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3276-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a3276-123">Child elements</span></span>

<span data-ttu-id="a3276-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a3276-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3276-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3276-125">Attributes</span></span>

|<span data-ttu-id="a3276-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a3276-126">**Attribute**</span></span>|<span data-ttu-id="a3276-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a3276-127">**Type**</span></span>|<span data-ttu-id="a3276-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a3276-128">**Required**</span></span>|<span data-ttu-id="a3276-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a3276-129">**Description**</span></span>|<span data-ttu-id="a3276-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a3276-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3276-131">ID</span><span class="sxs-lookup"><span data-stu-id="a3276-131">ID</span></span>  <br/> |<span data-ttu-id="a3276-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3276-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3276-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3276-133">required</span></span>  <br/> |<span data-ttu-id="a3276-134">Valor baseado em um que identifica o autor.</span><span class="sxs-lookup"><span data-stu-id="a3276-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="a3276-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a3276-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3276-136">Initials</span><span class="sxs-lookup"><span data-stu-id="a3276-136">Initials</span></span>  <br/> |<span data-ttu-id="a3276-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3276-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a3276-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a3276-138">optional</span></span>  <br/> |<span data-ttu-id="a3276-139">As iniciais do autor.</span><span class="sxs-lookup"><span data-stu-id="a3276-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="a3276-140">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a3276-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3276-141">Nome</span><span class="sxs-lookup"><span data-stu-id="a3276-141">Name</span></span>  <br/> |<span data-ttu-id="a3276-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3276-142">xsd:string</span></span>  <br/> |<span data-ttu-id="a3276-143">opcional</span><span class="sxs-lookup"><span data-stu-id="a3276-143">optional</span></span>  <br/> |<span data-ttu-id="a3276-144">O nome do autor.</span><span class="sxs-lookup"><span data-stu-id="a3276-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="a3276-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a3276-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3276-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="a3276-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="a3276-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3276-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a3276-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a3276-148">optional</span></span>  <br/> |<span data-ttu-id="a3276-149">Um identificador exclusivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="a3276-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="a3276-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a3276-150">Values of the xsd:string type.</span></span>  <br/> |
   

