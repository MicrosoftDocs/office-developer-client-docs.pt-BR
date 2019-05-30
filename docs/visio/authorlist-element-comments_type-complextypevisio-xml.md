---
title: Elemento authorlist (Comments_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica os autores de comentários em um desenho.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537854"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="37444-103">Elemento authorlist (Comments_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="37444-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="37444-104">Especifica os autores de comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="37444-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37444-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="37444-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37444-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="37444-106">**Element type**</span></span> <br/> |[<span data-ttu-id="37444-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="37444-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="37444-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37444-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="37444-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="37444-109">**Schema file**</span></span> <br/> |<span data-ttu-id="37444-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="37444-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="37444-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="37444-111">**Document parts**</span></span> <br/> |<span data-ttu-id="37444-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="37444-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37444-113">Definição</span><span class="sxs-lookup"><span data-stu-id="37444-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37444-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="37444-114">Elements and attributes</span></span>

<span data-ttu-id="37444-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="37444-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="37444-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="37444-116">Parent elements</span></span>

|<span data-ttu-id="37444-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37444-117">**Element**</span></span>|<span data-ttu-id="37444-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37444-118">**Type**</span></span>|<span data-ttu-id="37444-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37444-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37444-120">Comments</span><span class="sxs-lookup"><span data-stu-id="37444-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37444-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="37444-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37444-122">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="37444-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37444-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="37444-123">Child elements</span></span>

|<span data-ttu-id="37444-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37444-124">**Element**</span></span>|<span data-ttu-id="37444-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37444-125">**Type**</span></span>|<span data-ttu-id="37444-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37444-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37444-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="37444-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37444-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="37444-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37444-129">Especifica as propriedades que identificam o autor de um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="37444-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="37444-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="37444-130">Attributes</span></span>

<span data-ttu-id="37444-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37444-131">None.</span></span>
  

