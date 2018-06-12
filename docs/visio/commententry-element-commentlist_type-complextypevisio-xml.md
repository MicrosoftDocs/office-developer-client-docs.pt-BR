---
title: Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica as propriedades usadas para identificar um comentário em um desenho.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771535"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="c01db-103">Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c01db-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c01db-104">Especifica as propriedades usadas para identificar um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="c01db-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c01db-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c01db-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c01db-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c01db-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c01db-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c01db-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c01db-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c01db-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c01db-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c01db-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c01db-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c01db-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c01db-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c01db-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c01db-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="c01db-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c01db-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c01db-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c01db-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c01db-114">Elements and attributes</span></span>

<span data-ttu-id="c01db-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c01db-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c01db-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c01db-116">Parent elements</span></span>

|<span data-ttu-id="c01db-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c01db-117">**Element**</span></span>|<span data-ttu-id="c01db-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c01db-118">**Type**</span></span>|<span data-ttu-id="c01db-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c01db-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c01db-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="c01db-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c01db-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="c01db-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c01db-122">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="c01db-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c01db-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c01db-123">Child elements</span></span>

<span data-ttu-id="c01db-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c01db-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c01db-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="c01db-125">Attributes</span></span>

|<span data-ttu-id="c01db-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c01db-126">**Attribute**</span></span>|<span data-ttu-id="c01db-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c01db-127">**Type**</span></span>|<span data-ttu-id="c01db-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c01db-128">**Required**</span></span>|<span data-ttu-id="c01db-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c01db-129">**Description**</span></span>|<span data-ttu-id="c01db-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c01db-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c01db-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="c01db-131">AuthorID</span></span>  <br/> |<span data-ttu-id="c01db-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c01db-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c01db-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c01db-133">required</span></span>  <br/> |<span data-ttu-id="c01db-134">Um valor baseado em um que identifica o autor.</span><span class="sxs-lookup"><span data-stu-id="c01db-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="c01db-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c01db-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c01db-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="c01db-136">CommentID</span></span>  <br/> |<span data-ttu-id="c01db-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c01db-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c01db-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c01db-138">required</span></span>  <br/> |<span data-ttu-id="c01db-139">Um valor exclusivo que identifica o comentário em uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="c01db-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="c01db-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c01db-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c01db-141">Data</span><span class="sxs-lookup"><span data-stu-id="c01db-141">Date</span></span>  <br/> |<span data-ttu-id="c01db-142">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="c01db-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c01db-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c01db-143">required</span></span>  <br/> |<span data-ttu-id="c01db-144">Especifica que um comentário foi criado.</span><span class="sxs-lookup"><span data-stu-id="c01db-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="c01db-145">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="c01db-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="c01db-146">Concluído</span><span class="sxs-lookup"><span data-stu-id="c01db-146">Done</span></span>  <br/> |<span data-ttu-id="c01db-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="c01db-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c01db-148">opcional</span><span class="sxs-lookup"><span data-stu-id="c01db-148">optional</span></span>  <br/> |<span data-ttu-id="c01db-149">Especifica o estado atual do comentário.</span><span class="sxs-lookup"><span data-stu-id="c01db-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="c01db-150">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c01db-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c01db-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="c01db-151">EditDate</span></span>  <br/> |<span data-ttu-id="c01db-152">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="c01db-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c01db-153">opcional</span><span class="sxs-lookup"><span data-stu-id="c01db-153">optional</span></span>  <br/> |<span data-ttu-id="c01db-154">Especifica quando um comentário foi alterada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="c01db-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="c01db-155">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="c01db-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="c01db-156">PageID</span><span class="sxs-lookup"><span data-stu-id="c01db-156">PageID</span></span>  <br/> |<span data-ttu-id="c01db-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c01db-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c01db-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c01db-158">required</span></span>  <br/> |<span data-ttu-id="c01db-159">Um valor que identifica a página de desenho o comentário é no.</span><span class="sxs-lookup"><span data-stu-id="c01db-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="c01db-160">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c01db-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c01db-161">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="c01db-161">ShapeID</span></span>  <br/> |<span data-ttu-id="c01db-162">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c01db-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c01db-163">opcional</span><span class="sxs-lookup"><span data-stu-id="c01db-163">optional</span></span>  <br/> |<span data-ttu-id="c01db-164">Um valor que identifica de forma que o comentário é no.</span><span class="sxs-lookup"><span data-stu-id="c01db-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="c01db-165">Se nenhuma identificação da forma for especificada, o comentário refere-se à página de desenho.</span><span class="sxs-lookup"><span data-stu-id="c01db-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="c01db-166">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c01db-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

