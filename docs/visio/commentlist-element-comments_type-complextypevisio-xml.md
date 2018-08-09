---
title: Elemento CommentList (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica os comentários em um desenho.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771540"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="99919-103">Elemento CommentList (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="99919-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="99919-104">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="99919-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99919-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="99919-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99919-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="99919-106">**Element type**</span></span> <br/> |[<span data-ttu-id="99919-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="99919-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="99919-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="99919-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="99919-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="99919-109">**Schema file**</span></span> <br/> |<span data-ttu-id="99919-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="99919-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="99919-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="99919-111">**Document parts**</span></span> <br/> |<span data-ttu-id="99919-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="99919-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99919-113">Definição</span><span class="sxs-lookup"><span data-stu-id="99919-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="99919-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="99919-114">Elements and attributes</span></span>

<span data-ttu-id="99919-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="99919-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="99919-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="99919-116">Parent elements</span></span>

|<span data-ttu-id="99919-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99919-117">**Element**</span></span>|<span data-ttu-id="99919-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99919-118">**Type**</span></span>|<span data-ttu-id="99919-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99919-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99919-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="99919-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="99919-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="99919-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="99919-122">Especifica as propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="99919-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99919-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="99919-123">Child elements</span></span>

|<span data-ttu-id="99919-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99919-124">**Element**</span></span>|<span data-ttu-id="99919-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99919-125">**Type**</span></span>|<span data-ttu-id="99919-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99919-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99919-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="99919-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="99919-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="99919-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="99919-129">Especifica as propriedades usadas para identificar um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="99919-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="99919-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="99919-130">Attributes</span></span>

<span data-ttu-id="99919-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="99919-131">None.</span></span>
  

