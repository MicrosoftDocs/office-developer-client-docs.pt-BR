---
title: Comments_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542013"
---
# <a name="comments_type-complextype-visio-xml"></a><span data-ttu-id="685fa-102">Comments_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="685fa-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="685fa-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="685fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="685fa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="685fa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="685fa-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="685fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="685fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="685fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="685fa-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="685fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="685fa-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="685fa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="685fa-109">Definição</span><span class="sxs-lookup"><span data-stu-id="685fa-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="685fa-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="685fa-110">Elements and attributes</span></span>

<span data-ttu-id="685fa-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="685fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="685fa-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="685fa-112">Child elements</span></span>

|<span data-ttu-id="685fa-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="685fa-113">**Element**</span></span>|<span data-ttu-id="685fa-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="685fa-114">**Type**</span></span>|<span data-ttu-id="685fa-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="685fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="685fa-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="685fa-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="685fa-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="685fa-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="685fa-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="685fa-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="685fa-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="685fa-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="685fa-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="685fa-120">Attributes</span></span>

|<span data-ttu-id="685fa-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="685fa-121">**Attribute**</span></span>|<span data-ttu-id="685fa-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="685fa-122">**Type**</span></span>|<span data-ttu-id="685fa-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="685fa-123">**Required**</span></span>|<span data-ttu-id="685fa-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="685fa-124">**Description**</span></span>|<span data-ttu-id="685fa-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="685fa-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="685fa-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="685fa-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="685fa-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="685fa-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="685fa-128">opcional</span><span class="sxs-lookup"><span data-stu-id="685fa-128">optional</span></span>  <br/> ||<span data-ttu-id="685fa-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="685fa-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

