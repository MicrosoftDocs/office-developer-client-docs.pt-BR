---
title: Elemento Comments (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica propriedades usadas para identificar os autores e comentários em um desenho.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359392"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="51110-103">Elemento Comments (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="51110-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="51110-104">Especifica propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="51110-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51110-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="51110-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51110-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="51110-106">**Element type**</span></span> <br/> |[<span data-ttu-id="51110-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="51110-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="51110-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="51110-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="51110-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="51110-109">**Schema file**</span></span> <br/> |<span data-ttu-id="51110-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="51110-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="51110-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="51110-111">**Document parts**</span></span> <br/> |<span data-ttu-id="51110-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="51110-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="51110-113">Definição</span><span class="sxs-lookup"><span data-stu-id="51110-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="51110-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="51110-114">Elements and attributes</span></span>

<span data-ttu-id="51110-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="51110-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="51110-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="51110-116">Parent elements</span></span>

<span data-ttu-id="51110-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="51110-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51110-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="51110-118">Child elements</span></span>

|<span data-ttu-id="51110-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="51110-119">**Element**</span></span>|<span data-ttu-id="51110-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="51110-120">**Type**</span></span>|<span data-ttu-id="51110-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51110-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="51110-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="51110-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="51110-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="51110-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="51110-124">Especifica os autores em um desenho.</span><span class="sxs-lookup"><span data-stu-id="51110-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="51110-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="51110-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="51110-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="51110-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="51110-127">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="51110-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="51110-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="51110-128">Attributes</span></span>

<span data-ttu-id="51110-129">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="51110-129">None.</span></span>
  

