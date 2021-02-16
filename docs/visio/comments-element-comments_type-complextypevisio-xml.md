---
title: Elemento Comments (Comments_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica propriedades usadas para identificar os autores e comentários em um desenho.
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539217"
---
# <a name="comments-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="0187f-103">Elemento Comments (Comments_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="0187f-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0187f-104">Especifica propriedades usadas para identificar os autores e comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="0187f-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0187f-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="0187f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0187f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0187f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0187f-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="0187f-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0187f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0187f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0187f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0187f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0187f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0187f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0187f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="0187f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0187f-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="0187f-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0187f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="0187f-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0187f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0187f-114">Elements and attributes</span></span>

<span data-ttu-id="0187f-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0187f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0187f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0187f-116">Parent elements</span></span>

<span data-ttu-id="0187f-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0187f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0187f-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0187f-118">Child elements</span></span>

|<span data-ttu-id="0187f-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0187f-119">**Element**</span></span>|<span data-ttu-id="0187f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0187f-120">**Type**</span></span>|<span data-ttu-id="0187f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0187f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0187f-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="0187f-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0187f-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="0187f-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0187f-124">Especifica os autores em um desenho.</span><span class="sxs-lookup"><span data-stu-id="0187f-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="0187f-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="0187f-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0187f-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="0187f-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0187f-127">Especifica os comentários em um desenho.</span><span class="sxs-lookup"><span data-stu-id="0187f-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0187f-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="0187f-128">Attributes</span></span>

<span data-ttu-id="0187f-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0187f-129">None.</span></span>
  

