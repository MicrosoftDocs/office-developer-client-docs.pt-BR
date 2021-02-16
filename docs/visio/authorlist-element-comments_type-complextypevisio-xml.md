---
title: Elemento AuthorList (Comments_Type complexType) (XML do Visio)
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
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="900ec-103">Elemento AuthorList (Comments_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="900ec-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="900ec-104">Especifica os autores de comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="900ec-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="900ec-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="900ec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="900ec-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="900ec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="900ec-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="900ec-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="900ec-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="900ec-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="900ec-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="900ec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="900ec-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="900ec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="900ec-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="900ec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="900ec-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="900ec-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="900ec-113">Definição</span><span class="sxs-lookup"><span data-stu-id="900ec-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="900ec-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="900ec-114">Elements and attributes</span></span>

<span data-ttu-id="900ec-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="900ec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="900ec-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="900ec-116">Parent elements</span></span>

|<span data-ttu-id="900ec-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="900ec-117">**Element**</span></span>|<span data-ttu-id="900ec-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="900ec-118">**Type**</span></span>|<span data-ttu-id="900ec-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="900ec-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="900ec-120">Comments</span><span class="sxs-lookup"><span data-stu-id="900ec-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="900ec-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="900ec-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="900ec-122">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="900ec-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="900ec-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="900ec-123">Child elements</span></span>

|<span data-ttu-id="900ec-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="900ec-124">**Element**</span></span>|<span data-ttu-id="900ec-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="900ec-125">**Type**</span></span>|<span data-ttu-id="900ec-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="900ec-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="900ec-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="900ec-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="900ec-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="900ec-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="900ec-129">Especifica as propriedades que identificam o autor de um comentário em um desenho.</span><span class="sxs-lookup"><span data-stu-id="900ec-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="900ec-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="900ec-130">Attributes</span></span>

<span data-ttu-id="900ec-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="900ec-131">None.</span></span>
  

