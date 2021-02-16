---
title: Elemento CommentList (Comments_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica os comentários em um desenho.
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539245"
---
# <a name="commentlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="08ef1-103">Elemento CommentList (Comments_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="08ef1-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="08ef1-104">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="08ef1-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08ef1-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="08ef1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08ef1-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="08ef1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="08ef1-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="08ef1-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="08ef1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08ef1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="08ef1-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="08ef1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="08ef1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="08ef1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="08ef1-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="08ef1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="08ef1-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="08ef1-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08ef1-113">Definição</span><span class="sxs-lookup"><span data-stu-id="08ef1-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08ef1-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="08ef1-114">Elements and attributes</span></span>

<span data-ttu-id="08ef1-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="08ef1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="08ef1-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="08ef1-116">Parent elements</span></span>

|<span data-ttu-id="08ef1-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08ef1-117">**Element**</span></span>|<span data-ttu-id="08ef1-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08ef1-118">**Type**</span></span>|<span data-ttu-id="08ef1-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08ef1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08ef1-120">Comments</span><span class="sxs-lookup"><span data-stu-id="08ef1-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08ef1-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="08ef1-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="08ef1-122">Especifica propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="08ef1-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="08ef1-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="08ef1-123">Child elements</span></span>

|<span data-ttu-id="08ef1-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08ef1-124">**Element**</span></span>|<span data-ttu-id="08ef1-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08ef1-125">**Type**</span></span>|<span data-ttu-id="08ef1-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08ef1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08ef1-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="08ef1-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08ef1-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="08ef1-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="08ef1-129">Especifica propriedades usadas para identificar um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="08ef1-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="08ef1-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="08ef1-130">Attributes</span></span>

<span data-ttu-id="08ef1-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="08ef1-131">None.</span></span>
  

