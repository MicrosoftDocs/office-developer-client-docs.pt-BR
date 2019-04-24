---
title: Comments_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359406"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="a9b2b-102">Comments_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a9b2b-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a9b2b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="a9b2b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9b2b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a9b2b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a9b2b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a9b2b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a9b2b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a9b2b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a9b2b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a9b2b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a9b2b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a9b2b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a9b2b-110">Elements and attributes</span></span>

<span data-ttu-id="a9b2b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a9b2b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a9b2b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a9b2b-112">Child elements</span></span>

|<span data-ttu-id="a9b2b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-113">**Element**</span></span>|<span data-ttu-id="a9b2b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-114">**Type**</span></span>|<span data-ttu-id="a9b2b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a9b2b-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="a9b2b-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9b2b-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="a9b2b-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a9b2b-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="a9b2b-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9b2b-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="a9b2b-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a9b2b-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9b2b-120">Attributes</span></span>

|<span data-ttu-id="a9b2b-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-121">**Attribute**</span></span>|<span data-ttu-id="a9b2b-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-122">**Type**</span></span>|<span data-ttu-id="a9b2b-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-123">**Required**</span></span>|<span data-ttu-id="a9b2b-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-124">**Description**</span></span>|<span data-ttu-id="a9b2b-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a9b2b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a9b2b-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="a9b2b-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="a9b2b-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a9b2b-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a9b2b-128">opcional</span><span class="sxs-lookup"><span data-stu-id="a9b2b-128">optional</span></span>  <br/> ||<span data-ttu-id="a9b2b-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a9b2b-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

