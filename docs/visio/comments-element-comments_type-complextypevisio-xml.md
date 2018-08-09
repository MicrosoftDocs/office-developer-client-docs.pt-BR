---
title: Elemento de comentários (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica as propriedades usadas para identificar os autores e comentários em um desenho.
ms.openlocfilehash: 77695fb32aa88cb6c2b6ac5e9bff99fa12e262bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771536"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="6dfa5-103">Elemento de comentários (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6dfa5-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6dfa5-104">Especifica as propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6dfa5-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="6dfa5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dfa5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6dfa5-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="6dfa5-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6dfa5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6dfa5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6dfa5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6dfa5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6dfa5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6dfa5-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="6dfa5-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6dfa5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6dfa5-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6dfa5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6dfa5-114">Elements and attributes</span></span>

<span data-ttu-id="6dfa5-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6dfa5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6dfa5-116">Parent elements</span></span>

<span data-ttu-id="6dfa5-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6dfa5-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6dfa5-118">Child elements</span></span>

|<span data-ttu-id="6dfa5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-119">**Element**</span></span>|<span data-ttu-id="6dfa5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-120">**Type**</span></span>|<span data-ttu-id="6dfa5-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6dfa5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6dfa5-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="6dfa5-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6dfa5-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="6dfa5-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6dfa5-124">Especifica os autores em um desenho.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="6dfa5-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="6dfa5-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6dfa5-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="6dfa5-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6dfa5-127">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6dfa5-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="6dfa5-128">Attributes</span></span>

<span data-ttu-id="6dfa5-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dfa5-129">None.</span></span>
  

