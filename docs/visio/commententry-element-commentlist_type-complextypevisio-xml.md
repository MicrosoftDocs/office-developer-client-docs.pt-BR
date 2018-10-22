---
title: Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica propriedades usadas para identificar um comentário em um desenho.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397041"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="5c5ee-103">Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5c5ee-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5c5ee-104">Especifica propriedades usadas para identificar um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c5ee-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5c5ee-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c5ee-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5c5ee-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="5c5ee-107">CommentEntry_Type complexType</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5c5ee-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5c5ee-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5c5ee-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5c5ee-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5c5ee-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5c5ee-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="5c5ee-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c5ee-113">Definição</span><span class="sxs-lookup"><span data-stu-id="5c5ee-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c5ee-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5c5ee-114">Elements and attributes</span></span>

<span data-ttu-id="5c5ee-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5c5ee-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5c5ee-116">Parent elements</span></span>

|<span data-ttu-id="5c5ee-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-117">**Element**</span></span>|<span data-ttu-id="5c5ee-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-118">**Type**</span></span>|<span data-ttu-id="5c5ee-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c5ee-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="5c5ee-120">CommentList element</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5c5ee-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="5c5ee-121">CommentList_Type complexType</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c5ee-122">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c5ee-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5c5ee-123">Child elements</span></span>

<span data-ttu-id="5c5ee-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c5ee-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c5ee-125">Attributes</span></span>

|<span data-ttu-id="5c5ee-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-126">**Attribute**</span></span>|<span data-ttu-id="5c5ee-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-127">**Type**</span></span>|<span data-ttu-id="5c5ee-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-128">**Required**</span></span>|<span data-ttu-id="5c5ee-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-129">**Description**</span></span>|<span data-ttu-id="5c5ee-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5c5ee-130">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c5ee-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="5c5ee-131">AuthorID</span></span>  <br/> |<span data-ttu-id="5c5ee-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c5ee-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c5ee-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5c5ee-133">required</span></span>  <br/> |<span data-ttu-id="5c5ee-134">Valor baseado em um que identifica o autor.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="5c5ee-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="5c5ee-136">CommentID</span></span>  <br/> |<span data-ttu-id="5c5ee-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c5ee-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c5ee-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5c5ee-138">required</span></span>  <br/> |<span data-ttu-id="5c5ee-139">Um valor exclusivo que identifica o comentário em uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="5c5ee-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-141">Date</span><span class="sxs-lookup"><span data-stu-id="5c5ee-141">Date</span></span>  <br/> |<span data-ttu-id="5c5ee-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="5c5ee-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5c5ee-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5c5ee-143">required</span></span>  <br/> |<span data-ttu-id="5c5ee-144">Especifica quando um comentário foi criado.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="5c5ee-145">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-146">Done</span><span class="sxs-lookup"><span data-stu-id="5c5ee-146">Done</span></span>  <br/> |<span data-ttu-id="5c5ee-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5c5ee-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5c5ee-148">opcional</span><span class="sxs-lookup"><span data-stu-id="5c5ee-148">optional</span></span>  <br/> |<span data-ttu-id="5c5ee-149">Especifica o estado atual do comentário.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="5c5ee-150">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="5c5ee-151">EditDate Property</span></span>  <br/> |<span data-ttu-id="5c5ee-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="5c5ee-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5c5ee-153">opcional</span><span class="sxs-lookup"><span data-stu-id="5c5ee-153">optional</span></span>  <br/> |<span data-ttu-id="5c5ee-154">Especifica quando um comentário foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="5c5ee-155">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-156">PageID</span><span class="sxs-lookup"><span data-stu-id="5c5ee-156">expression  . PageID</span></span>  <br/> |<span data-ttu-id="5c5ee-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c5ee-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c5ee-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5c5ee-158">required</span></span>  <br/> |<span data-ttu-id="5c5ee-159">Um valor que identifica a página de desenho em que o comentário está ativo.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="5c5ee-160">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c5ee-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="5c5ee-161">ShapeId</span></span>  <br/> |<span data-ttu-id="5c5ee-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c5ee-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c5ee-163">opcional</span><span class="sxs-lookup"><span data-stu-id="5c5ee-163">optional</span></span>  <br/> |<span data-ttu-id="5c5ee-164">Um valor que identifica a forma em que o comentário está.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="5c5ee-165">Se nenhum ShapeID for especificado, o comentário se refere à página de desenho.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="5c5ee-166">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

