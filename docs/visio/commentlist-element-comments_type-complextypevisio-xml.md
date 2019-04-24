---
title: Elemento CommentList (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica os comentários em um desenho.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359427"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="be128-103">Elemento CommentList (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="be128-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="be128-104">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="be128-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be128-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="be128-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be128-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="be128-106">**Element type**</span></span> <br/> |[<span data-ttu-id="be128-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="be128-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="be128-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be128-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="be128-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="be128-109">**Schema file**</span></span> <br/> |<span data-ttu-id="be128-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="be128-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="be128-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="be128-111">**Document parts**</span></span> <br/> |<span data-ttu-id="be128-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="be128-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be128-113">Definição</span><span class="sxs-lookup"><span data-stu-id="be128-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be128-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="be128-114">Elements and attributes</span></span>

<span data-ttu-id="be128-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="be128-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="be128-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="be128-116">Parent elements</span></span>

|<span data-ttu-id="be128-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be128-117">**Element**</span></span>|<span data-ttu-id="be128-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="be128-118">**Type**</span></span>|<span data-ttu-id="be128-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be128-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be128-120">Comments</span><span class="sxs-lookup"><span data-stu-id="be128-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be128-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="be128-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be128-122">Especifica propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="be128-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="be128-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="be128-123">Child elements</span></span>

|<span data-ttu-id="be128-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be128-124">**Element**</span></span>|<span data-ttu-id="be128-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="be128-125">**Type**</span></span>|<span data-ttu-id="be128-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be128-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be128-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="be128-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be128-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="be128-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be128-129">Especifica propriedades usadas para identificar um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="be128-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="be128-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="be128-130">Attributes</span></span>

<span data-ttu-id="be128-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="be128-131">None.</span></span>
  

