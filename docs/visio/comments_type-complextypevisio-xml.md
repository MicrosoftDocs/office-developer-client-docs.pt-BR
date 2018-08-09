---
title: Comments_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: 4d7a1d75387ddc84bec8eb1370cfb7d641c8a9ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771542"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="6e94e-102">Comments_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6e94e-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6e94e-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="6e94e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e94e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6e94e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6e94e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6e94e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6e94e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6e94e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6e94e-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="6e94e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6e94e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6e94e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e94e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6e94e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6e94e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6e94e-110">Elements and attributes</span></span>

<span data-ttu-id="6e94e-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6e94e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6e94e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6e94e-112">Child elements</span></span>

|<span data-ttu-id="6e94e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e94e-113">**Element**</span></span>|<span data-ttu-id="6e94e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e94e-114">**Type**</span></span>|<span data-ttu-id="6e94e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e94e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e94e-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="6e94e-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e94e-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="6e94e-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6e94e-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="6e94e-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e94e-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="6e94e-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6e94e-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e94e-120">Attributes</span></span>

|<span data-ttu-id="6e94e-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6e94e-121">**Attribute**</span></span>|<span data-ttu-id="6e94e-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e94e-122">**Type**</span></span>|<span data-ttu-id="6e94e-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6e94e-123">**Required**</span></span>|<span data-ttu-id="6e94e-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e94e-124">**Description**</span></span>|<span data-ttu-id="6e94e-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6e94e-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6e94e-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="6e94e-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="6e94e-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6e94e-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6e94e-128">opcional</span><span class="sxs-lookup"><span data-stu-id="6e94e-128">optional</span></span>  <br/> ||<span data-ttu-id="6e94e-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6e94e-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

