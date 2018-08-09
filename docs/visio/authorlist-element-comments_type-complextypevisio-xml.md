---
title: Elemento AuthorList (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica os autores de comentários em um desenho.
ms.openlocfilehash: 0f31e11e52809df60b41cb67b868b15435e0eb47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771307"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="3a63d-103">Elemento AuthorList (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3a63d-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3a63d-104">Especifica os autores de comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="3a63d-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a63d-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="3a63d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a63d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3a63d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3a63d-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="3a63d-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3a63d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3a63d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3a63d-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3a63d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3a63d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3a63d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3a63d-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="3a63d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3a63d-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="3a63d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3a63d-113">Definição</span><span class="sxs-lookup"><span data-stu-id="3a63d-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3a63d-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3a63d-114">Elements and attributes</span></span>

<span data-ttu-id="3a63d-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3a63d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3a63d-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3a63d-116">Parent elements</span></span>

|<span data-ttu-id="3a63d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a63d-117">**Element**</span></span>|<span data-ttu-id="3a63d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a63d-118">**Type**</span></span>|<span data-ttu-id="3a63d-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a63d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3a63d-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="3a63d-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a63d-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="3a63d-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3a63d-122">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="3a63d-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3a63d-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3a63d-123">Child elements</span></span>

|<span data-ttu-id="3a63d-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a63d-124">**Element**</span></span>|<span data-ttu-id="3a63d-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a63d-125">**Type**</span></span>|<span data-ttu-id="3a63d-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a63d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3a63d-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="3a63d-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a63d-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3a63d-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3a63d-129">Especifica as propriedades que identificam o autor de um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="3a63d-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3a63d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a63d-130">Attributes</span></span>

<span data-ttu-id="3a63d-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3a63d-131">None.</span></span>
  

